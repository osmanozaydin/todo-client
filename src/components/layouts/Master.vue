<template>
    <div id="app">
        <ul class="nav">
            <li><router-link :to="{name: 'home'}">Anasayfa</router-link></li>
            <li><router-link :to="{name: 'todo'}">Todo</router-link></li>
            <li><router-link :to="{name: 'about'}">Hakkımızda</router-link></li>
            <li><router-link :to="{name: 'login'}">Giriş</router-link></li>
            <li><router-link :to="{name: 'register'}">Kayıt</router-link></li>
        </ul>
    <div>
           <router-view></router-view>
    </div>


    </div>
</template>
<script>
export default {
    
}
</script>

<style>
*{
    box-sizing: border-box;
    margin:0;
    padding: 0;
}
#app{
    font-family: 'Avenir', Arial, Helvetica, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    font-size: 24px;
    height: 100vh;
}
.flex-center {
    display: flex;
    justify-content: center;
}
.nav{
    display: flex;
    list-style: none;
    padding: 15px 0;
    margin: 0;
    justify-content: flex-end;
    background:  #53b6b2;
    border-bottom: 1px solid #15284c;
    margin-bottom: 24px;
}
.nav a {
    color: white;
    padding: 0 25px;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: .1rem;
    text-decoration: none;
    text-transform: uppercase;
}
.nav a:hover {
  color: #15284c;
}
</style>