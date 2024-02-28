<script>
import Header from './components/Header.vue'
import News from './components/pages/News.vue' // TODO: remove
import Footer from './components/Footer.vue'

export default {
  
  components: {
    Header,
    News,
    Footer
  }
}
</script>

<template>
  <Header />
  <News />
  <Footer />
</template>

<style>
</style>
