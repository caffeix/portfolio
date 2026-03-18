<script setup lang="ts">
  import Header from "./components/Header.vue";
  import AboutMe from "./components/AboutMe.vue";
  import Footer from "./components/Footer.vue";
  import { navItems } from "./data/navItems";
  import { profile } from "./data/profile";
</script>

<template>
  <div class="wrapper">
    <Header :navItems="navItems" />
    <AboutMe :profile="profile" />
    <Footer />
  </div>
</template>

<style>
  .wrapper {
    max-height: 100vh;
    margin: 0 auto;
    width: 100%;
  }
</style>