<script setup lang="ts">

const alt = 'dummy';
</script>
<template>
  <div id="about">
    <picture>
      <source type="image/webp" srcset="@/assets/dummy.png?preset=img&format=webp&srcset">
      <img src="@/assets/dummy.png?preset=img&src" srcset="@/assets/dummy.png?preset=img&srcset"  :alt="alt"/>
    </picture>
  </div>
</template>
<style scoped lang="scss">
#about{
  text-align: center;
  img{
    width: 100%;
    max-width: 700px;
    object-fit: contain;
  }
}
</style>
