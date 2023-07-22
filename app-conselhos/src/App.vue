<script setup>
import HeaderDefault from './components/HeaderDefault.vue';
</script>
<template>
  <link href="assets/my-style.css" rel="stylesheet">
  <HeaderDefault/>
  <RouterView class="main" />
</template>

<style scoped>
.main {
  height: 49rem;
}
</style>
