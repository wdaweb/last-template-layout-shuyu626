<template>
  <v-app>
    <v-main>
      <Navbar/>
      <AppCarousel />
      <MainInfo1/>
      <MainInfo2/>
      <MainInfo3/>
      <MainInfo4/>
    </v-main>

    <AppFooter />
  </v-app>
</template>

<script setup>
import Navbar from '../components/NavBar.vue'
import AppCarousel from '../components/AppCarousel.vue'
import MainInfo1 from '../components/MainInfo1.vue'
import MainInfo2 from '../components/MainInfo2.vue'
import MainInfo3 from '../components/MainInfo3.vue'
import MainInfo4 from '../components/MainInfo4.vue'
</script>
<style>
   .title-size{
    font-size: 13px;
  }
  .border-1{
    border: 1px solid black;
  }
  .border-bottom{
    border-bottom: 1px solid black;
  }
</style>
