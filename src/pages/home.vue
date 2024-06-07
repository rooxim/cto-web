<script setup lang="ts">
import headerArea from '@/components/header.vue'
import mainArea from '@/components/main.vue'
import Footer from '@/components/footer.vue';
import MainMessage from '@/components/mainMessage.vue';
import Worry from '@/components/worry.vue';
import Advantages from '@/components/advantages.vue';
import Prices from '@/components/prices.vue';
import Contact from "@/components/contact.vue";
import ActionMenu from "@/components/ActionMenu.vue";
import How from "@/components/how.vue";
</script>
<template>
  <v-app>
  <headerArea/>
  <mainArea/>
  <main-message/>
  <prices/>
  <how/>
  <worry/>
  <advantages/>
  <contact/>
  <Footer />
  <action-menu />
  </v-app>
</template>

<style scoped lang="scss">
</style>
