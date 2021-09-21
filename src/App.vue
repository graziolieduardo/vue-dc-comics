<template>
  <div id="app">
      <Header />
      <main>
        <Jumbotron />
        <Products />
        <Main />
      </main>
      <Footer />  
    </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Products from './components/Products.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Products,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import '@/assets/style/general';

</style>
