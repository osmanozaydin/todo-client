<template>
  <div>{{ remaining }} iş var</div>
</template>

<script>
export default {
  name: 'todo-remaining',
  computed: {
    remaining() {
      return this.$store.getters.remaining
    }
  }
}
</script>

