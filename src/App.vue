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
  // overflow-y: hidden;
}
html,body{
  overflow: hidden;
}
#app {
  font-family: 'neon', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  overflow-x: scroll;
  display: flex;
}

@font-face {
  font-family: neon;
  src: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/707108/neon.ttf);
}
</style>