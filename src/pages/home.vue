<script setup lang="ts">
import headerArea from '@/components/header.vue'
import mainArea from '@/components/main.vue'
import Footer from '@/components/footer.vue';
import MainMessage from '@/components/mainMessage.vue';
import Worry from '@/components/worry.vue';
import Advantages from '@/components/advantages.vue';
import Prices from '@/components/prices.vue';
</script>
<template>
  <div class="root">
    <headerArea/>
    <mainArea/>
    <main-message/>
    <advantages/>
    <worry/>
    <prices/>
<!--    <Access />-->
    <Footer />
<!--    <action-menu />-->
  </div>
</template>

<style scoped lang="scss">
.root{
  padding-bottom: 10px;
  width: 100svw;
}
</style>
