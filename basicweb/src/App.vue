<template>
  <Registration />
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Registration from './components/Registration.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Registration
  }
}
</script>

<style>
html, body {
  width: 100%;
  height: 100%;
  margin: 0px;
  padding: 0px;
}


body {
  background-image: url("./assets/bg.png");
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
}
</style>
