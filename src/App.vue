<template>
  <div id="app">
    <Landing class=""></Landing>
    <Page></Page>
  </div>
</template>

<script>
import Page from './components/Page.vue'
import Landing from './components/Landing.vue'

export default {
  name: 'app',
  components: {
    Page,
    Landing
  }
}
</script>

<style lang="scss" scope>
*,*::before,*::after {
  margin: 0;
  padding: 0;
}
html,body{
  overflow: hidden;
  width: 100%;
  height: 100%;
}
#app {
  width: 100%;
  height: 100%;
  font-family: 'neon', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  scroll-behavior: smooth;
  overflow-x: scroll;
  display: flex;
  
}

@font-face {
  font-family: neon;
  src: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/707108/neon.ttf);
}
</style>