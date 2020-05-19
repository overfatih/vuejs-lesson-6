<template>
  <div class="container">
    <Header/>
    <hr>
    <ServerList/>
    <hr>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header'
import ServerList from './components/ServerList'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Header,
    ServerList,
    Footer
  }
}
</script>

<style>

</style>
