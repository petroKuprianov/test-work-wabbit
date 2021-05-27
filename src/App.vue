<template>
  <div id="app">
    <Header></Header>
    <about></about>
    <services></services>
    <main-page></main-page>
    <news></news>
    <footer-comp></footer-comp>
  </div>
</template>

<script>

import Header from './components/header'
import About from './components/about'
import Services from './components/services'
import MainPage from './components/main'
import News from './components/news'
import FooterComp from './components/footer-component'

export default {
  name: 'App',
  components: {
    Header,
    About,
    Services,
    MainPage,
    News,
    FooterComp
  }
}
</script>

<style>
@font-face {
  font-family: 'Inter';
  src: url('./assets/fonts/Inter-Medium.ttf');
}

body{
  padding: 0;
  margin: 0;
}
</style>

