<script setup lang="ts">
import Line from '@/components/atoms/line.vue';
import Mail from "@/components/atoms/mail.vue";
import {onMounted, ref} from "vue";

const small = ref(false);

const onResize = ()=>{
  small.value = window.innerWidth <= 600;
}

onMounted(()=>{
  window.addEventListener('resize', onResize);
  onResize();
  return ()=>{
    window.removeEventListener('resize', onResize);
  }
});


</script>
<template>
    <v-app-bar fixed>
      <v-app-bar-title>あなたの組織のCTO</v-app-bar-title>
      <template v-slot:append v-if="small===false">
        <div class="append">
<!--          <Line/>-->
          <Mail/>
        </div>
      </template>
      <template v-slot:extension v-if="small===true">
        <div class="extension">
          <div class="append">
<!--            <Line/>-->
            <Mail/>
          </div>
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
  justify-content: end;
  width: 350px;

  @media screen and (max-width: 360px){
    flex-direction: column;
    width: 100%;
    height: 80px;
  }
}
.v-toolbar__content{
  @media screen and (max-width: 600px){
    height: 100px !important;
  }
}

.extension{
  width: 100%;
  .append{
    margin-right: auto;
    margin-left: auto;
  }
}
</style>
