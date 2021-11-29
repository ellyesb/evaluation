<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  <label for="start">Start date:</label>

<input type="date" id="start" name="trip-start"
       value="date"
       min="2018-01-01" max="2018-12-31">
  <p>Select a maintenance drone:</p>

<div>
  <input type="radio" id="13h30" name="drone" value="heure"
         checked>
  <label for="13h30">13h30</label>
</div>

<div>
  <input type="radio" id="14h30" name="drone" value="heure">
  <label for="14h30">14h30</label>
</div>

<div>
  <input type="radio" id="15h30" name="drone" value="heure">
  <label for="15h30">15h30</label>
</div>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
