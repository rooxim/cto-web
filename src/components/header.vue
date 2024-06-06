<template>
    <v-app-bar>
      <v-app-bar-title>あなたの組織のCTO</v-app-bar-title>
      <template v-slot:append>
        <Line/>
      </template>
    </v-app-bar>
    <div class="dummy_space">

    </div>
</template>

<style scoped lang="scss">
.dummy_space {
  height: 60px;
}
</style>
<script setup lang="ts">

import Line from '@/components/atoms/line.vue';
</script>
