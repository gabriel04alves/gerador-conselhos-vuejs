<script setup>
import FooterDefault from './components/FooterDefault.vue';
import HeaderDefault from './components/HeaderDefault.vue';
</script>
<template>
  <link href="assets/my-style.css" rel="stylesheet">
  <HeaderDefault/>
  <RouterView class="router-view" />
  <FooterDefault/>
</template>

<style scoped>
</style>
