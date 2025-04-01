<script setup>
  import Navbar from "@/components/Navbar.vue";
  import data from "../public/portfolio.js"

</script>

<template>
  <Navbar />
  <router-view :data="data" />
</template>

<style scoped lang="scss">

</style>
