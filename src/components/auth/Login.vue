<template>
<div class="login-form flex-center">
  <div class="login-page">
  <div class="form">
    <form class="login-form" action="" @submit.prevent="login">
      <input type="text" name="username" placeholder="Email" v-model="username"/>
      <input type="password" name="password" placeholder="Şifre" v-model="password"/>
      <button type="submit" >Giriş Yap</button>
    </form>
  </div>
</div>
</div>

</template>
<script>
export default {
    name: 'login',
    data() {
        return {
        username: '',
        password: '',
    }
},
methods: {
    login() {
        this.$store.dispatch('retrieveToken', {
            username: this.username,
            password: this.password,
        })
    }
}
}
</script>
<style>
@import url(https://fonts.googleapis.com/css?family=Roboto:300);

.login-page {
  width: 360px;
  padding: 8% 0 0;
  margin: auto;
}
.form {
  position: relative;
  z-index: 1;
  background: #FFFFFF;
  max-width: 360px;
  margin: 0 auto 100px;
  padding: 45px;
  text-align: center;
  box-shadow: 0 0 20px 0 rgba(0, 0, 0, 0.2), 0 5px 5px 0 rgba(0, 0, 0, 0.24);
}
.form input {
  font-family: "Roboto", sans-serif;
  outline: 0;
  background: #f2f2f2;
  width: 100%;
  border: 0;
  margin: 0 0 15px;
  padding: 15px;
  box-sizing: border-box;
  font-size: 14px;
}
.form button {
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  outline: 0;
  background: #53b6b2;
  width: 100%;
  border: 0;
  padding: 15px;
  color: #FFFFFF;
  font-size: 14px;
  -webkit-transition: all 0.3 ease;
  transition: all 0.3 ease;
  cursor: pointer;
}
.form button:hover,.form button:active,.form button:focus {
  background: #53b6c5;
}

body {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;      
}
</style>