<template>
    <v-app-bar>
      <v-app-bar-title>あなたの組織のCTO</v-app-bar-title>
      <template v-slot:append>
        <div class="append">
          <Line/>
          <Mail/>
        </div>
      </template>
    </v-app-bar>
    <div class="dummy_space">

    </div>
</template>

<style scoped lang="scss">
.dummy_space {
  height: 60px;
}
.append{
  display: flex;
  justify-content: space-between;
  width: 360px;
}
</style>
<script setup lang="ts">

import Line from '@/components/atoms/line.vue';
import Mail from "@/components/atoms/mail.vue";
</script>
