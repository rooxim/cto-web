<script setup lang="ts">
import Line from "@/components/atoms/line.vue";

</script>
<template>
  <v-container id="join">
    <h1>お申し込み</h1>
    <div>9,800円/月</div>
    <Line />
    <table>
      <tr>
        <td></td>
      </tr>
    </table>
  </v-container>
</template>
<style scoped lang="scss">
#join{
  text-align: center;
  img{
    width: 100%;
    max-width: 700px;
    object-fit: contain;
  }
}
</style>
