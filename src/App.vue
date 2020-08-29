<template>
  <div id="app" class="container">
    <img alt="Vue logo" class="logo" src="./assets/logo.png">
    <todo msg="Simple todo app"/>
  </div>
</template>

<script>
import Todo from './components/Todo'

export default {
  name: 'App',
  components: {
    Todo
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
.container {
  width: 400px;
  margin: 0 auto;
}
.logo { 
  height: 100px;
}
</style>
