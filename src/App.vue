<template>
  <div id="app">
    <loader-box v-if="!loaded"/>
    <div v-else>
      <header-box />
      <select-box @selectArray="filterArray" @authorArray="authorArray" />
      <main-container :discs="discsList" />
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import MainContainer from './components/MainContainer.vue'
import HeaderBox from './components/HeaderBox'
import LoaderBox from './components/LoaderBox.vue'
import SelectBox from './components/SelectBox.vue'


export default {
  name: 'App',
  components: {
    MainContainer,
    HeaderBox,
    LoaderBox,
    SelectBox,
  }, data() {
    return {
      discsListSource: '[]',
      discsList: '[]',
      loaded: false,
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.discsListSource = response.data.response;
      this.discsList = response.data.response;
      this.loaded = true;
    } )
  },
  methods: {
    filterArray (keyword) {
      this.discsList = this.discsListSource;
      this.discsList = this.discsListSource.filter((element) => element.genre.includes(keyword))
    },
    authorArray (keyword) {
      this.discsList = this.discsListSource;
      this.discsList = this.discsListSource.filter((element) => element.author.includes(keyword))
    }
  },
}
</script>

<style lang="scss">
@import '@/style/main.scss'
</style>
