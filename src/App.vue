<template>
  <div id="app">
    <Header/>
    <MusicList/>
  </div>
</template>

<script>
import MusicList from './components/MusicList.vue'
import Header from './components/Header.vue'



export default {
  name: 'App',
  components: {
    Header,
    MusicList
  }
}
</script>

<style lang="scss">

* {
  margin: 0;
  padding: 0;
  border: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
