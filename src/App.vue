<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Content.vue';

export default {
  name: 'app',
  components: {
    Header,
    Main
  },
};
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Kanit:200,300,400,600');
  body, html {
    margin: 0px;
    padding: 0px;

  }
  #app {
    font-family: 'Kanit', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    width: 100%;
  }
</style>
