<script setup>
  import Header from './components/Header/Header.vue'
  import HomeView from './views/HomeView.vue';
  import Footer from './components/Footer/Footer.vue';
</script>

<template>
  <Header/>
  <router-view></router-view>
  <Footer/>
</template>

<style scoped>

</style>
