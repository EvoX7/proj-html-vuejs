<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header/Header.vue'
import Main from './components/Main/Main.vue'
import Footer from './components/Footer/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  
  }
}
</script>

<style lang="scss">
// Ubuntu font 
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@700&display=swap');
@import "~bootstrap/scss/bootstrap.scss";
@import "./style/variables.scss";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
