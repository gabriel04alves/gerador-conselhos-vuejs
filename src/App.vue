<script setup>
import FooterDefault from './components/FooterDefault.vue';
import HeaderDefault from './components/HeaderDefault.vue';
</script>
<template>
  <HeaderDefault/>
  <RouterView class="router-view" />
  <FooterDefault/>
</template>

<style scoped>
</style>
