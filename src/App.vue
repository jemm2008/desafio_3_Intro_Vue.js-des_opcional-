<template>
  <div id="app">
    <Users_table/>
  </div>
</template>

<script>
import Users_table from './components/Users_table.vue'

export default {
  name: 'App',
  components: {
    Users_table
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
