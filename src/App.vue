<template>
  <div id="app">
    <header-box />
    <main-container :discs="discsList" />
  </div>
</template>

<script>
import axios from 'axios'
import MainContainer from './components/MainContainer.vue'


export default {
  name: 'App',
  components: {
    MainContainer,
  }, data() {
    return {
      discsList: '[]',
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.discsList = response.data;
    } )
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
