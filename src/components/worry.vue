<script setup lang="ts">
import webp from "@/assets/dummy.png?preset=img&format=webp&srcset";
import img from "@/assets/dummy.png?preset=img&src";
import srcset from "@/assets/dummy.png?preset=img&srcset";

const items = [
  {
    images:{
      webp,
      img,
      srcset,
    },
    message: 'メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ'
  },{
    images:{
      webp,
      img,
      srcset,
    },
    message: 'メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ'
  },
  {
    images:{
      webp,
      img,
      srcset,
    },
    message: 'メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ'
  },
  {
    images:{
      webp,
      img,
      srcset,
    },
    message: 'メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ　メッセージ'
  }
]
</script>
<template>
  <div id="worry">
    <h1>こんな悩みありませんか？</h1>

    <div class="itemsArea">
      <div class="items">
        <div class="item" v-for="item in items">
          <picture>
            <source type="image/webp" :srcset="item.images.webp" />
            <img :src="item.images.img" :srcset="item.images.srcset" alt="dummy" />
          </picture>
          <div class="message">
            {{item.message}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.itemsArea{
  padding: 20px;
  background-color: #dfdfdf;
  display: flex;
  justify-content: center;
  align-items: center;
}
.items{
  max-width: 1024px;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;

  .item{
    flex-basis: 32%;
    background-color: #ffffff;
    padding: 10px;
    margin: 5px 0;

    display: flex;

    img{
      border-radius: 10px;
      width: 80px;
      height: 80px;
    }

    .message{
      padding: 0 5px;
      font-size: 14px;
    }
  }
  @media screen and (max-width: 900px) {
    .item{
      flex-basis: 49%;
    }
  }

  @media screen and (max-width: 600px) {
    .item{
      flex-basis: 100%;
    }
  }
}

</style>
