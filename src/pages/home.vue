<script setup lang="ts">
import headerArea from '../components/header.vue'
import mainArea from '../components/main.vue'
import Footer from '../components/footer.vue';
import ActionMenu from '../components/ActionMenu.vue'
import MainMessage from "../components/mainMessage.vue";
import Worry from "../components/worry.vue";
import About from "../components/about.vue";
</script>
<template>
  <div class="root">
    <headerArea/>
    <mainArea/>
    <main-message/>
    <about/>
    <worry/>
<!--    <Access />-->
    <Footer />
    <action-menu />
  </div>
</template>

<style scoped lang="scss">
.root{
  padding-bottom: 10px;
  width: 100svw;
}
</style>
