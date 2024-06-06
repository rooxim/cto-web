<script lang="ts" setup>

</script>
<template>
  <v-btn class="btn">
    <picture class="btn-img">
      <source type="image/webp" srcset="@/assets/line.png?preset=img&format=webp&srcset">
      <img class="btn-img" src="@/assets/line.png?preset=img&src" srcset="@/assets/line.png?preset=img&srcset" alt="alt" />
    </picture>
    <div>Lineで申し込み</div>
  </v-btn>
</template>
<style scoped lang="scss">
.btn{
  background-color: #03C755;
  color: #fff;
  .v-btn__content{
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
.btn-img{
  height: 25px;
  width: 25px;
}
</style>
