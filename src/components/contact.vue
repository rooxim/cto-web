<script setup lang="ts">
import Mail from "@/components/atoms/mail.vue";
import Line from "@/components/atoms/line.vue";
</script>
<template>
  <v-container id="contact">
    <h1>お問い合わせ</h1>
    <div>まずはお気軽にお問い合わせください。</div>
    <Line/> <Mail/>
  </v-container>
</template>
<style scoped lang="scss">
#contact{
  text-align: center;
  img{
    width: 100%;
    max-width: 700px;
    object-fit: contain;
  }
}
</style>
