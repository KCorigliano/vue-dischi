<template>
  <div id="app">
    <loader-box v-if="!loaded"/>
    <div v-else>
      <header-box />
      <main-container :discs="discsList" />
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import MainContainer from './components/MainContainer.vue'
import HeaderBox from './components/HeaderBox'
import LoaderBox from './components/LoaderBox.vue'


export default {
  name: 'App',
  components: {
    MainContainer,
    HeaderBox,
    LoaderBox,
  }, data() {
    return {
      discsList: '[]',
      loaded: false,
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.discsList = response.data.response;
      this.loaded = true;
    } )
  }
}
</script>

<style lang="scss">
@import '@/style/main.scss'
</style>
