<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <SimpleTextInput :value="value" @input="value = $event" />
    {{ value }}
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import SimpleTextInput from "./components/SimpleTextInput.vue"

export default {
  name: 'App',
  components: {
    HelloWorld,
    SimpleTextInput
  },
  data() {
    return {
      value: ""
    }
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
