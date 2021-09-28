<template>
  <div id="app">
    <EmailList />
  </div>
</template>

<script>
import EmailList from './components/email-list.vue'

export default {
  name: 'App',
  components: {
    EmailList
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  
  
}
</style>
