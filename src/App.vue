// -------------------------------
// HTML

<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

// -------------------------------
// JS

<script>
import Header from './components/MainHeader.vue'
import Main from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

// -------------------------------
// CSS

<style lang="scss">

@import './assets/scss/_common.scss';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

</style>
