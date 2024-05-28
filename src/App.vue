<script setup lang="ts">
import { useRoute } from 'vue-router'
const route = useRoute()

console.log('path',route.fullPath, route.name);
</script>
<template>
  <router-view />
</template>
