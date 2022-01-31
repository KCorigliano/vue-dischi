<template>
  <div id="app">
    <header-box />
    <main-container :discs="discsList" />
  </div>
</template>

<script>
import axios from 'axios'
import MainContainer from './components/MainContainer.vue'
import HeaderBox from './components/HeaderBox'


export default {
  name: 'App',
  components: {
    MainContainer,
    HeaderBox
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
@import '@/style/main.scss'
</style>
