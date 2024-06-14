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
<!--          <div><Line/></div>-->
          <div><Mail/></div>

        </div>
      </template>
      <template v-slot:extension v-if="small===true">
        <div class="extension">
          <div class="append">
<!--            <div><Line/></div>-->
            <div><Mail/></div>
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


  div{
    margin-left: 10px;
  }
}

.extension{
  width: 100%;

  .append{
    margin-right: auto;
    margin-left: auto;

    flex-direction: row;
    justify-content: center;
    align-items: center;


    width: 100%;

    div{
      padding: 10px 0;
    }

    @media screen and (max-width: 400px){
      flex-direction: column;

      div{
        padding: 2px 0;
      }

    }
  }
}

//:deep(.v-toolbar__extension){
//  @media screen and (max-width: 400px){
//    height: 90px !important;
//  }
//}
</style>
