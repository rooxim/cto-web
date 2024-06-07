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
    title: '相見積もりを取って開発したけれど、プロジェクトが失敗した。',
    message: ''
  },{
    images:{
      webp,
      img,
      srcset,
    },
    title: 'システムを使ったサービスを始めたいけどなにをしたらいいかわからない。',
    message: ''
  },
  {
    images:{
      webp,
      img,
      srcset,
    },
    title: 'エンジニアに開発をお願いしているが何を言っているかわからない。',
    message: ''
  },
  {
    images:{
      webp,
      img,
      srcset,
    },
    title: '技術選定をしたが、本当に問題ないか不安',
    message: ''
  }
]
</script>
<template>
  <v-container id="worry">
    <h1>こんな悩みありませんか？</h1>

    <div class="itemsArea">
      <div class="items">
        <div class="item" v-for="item in items">
          <picture>
            <source type="image/webp" :srcset="item.images.webp" />
            <img :src="item.images.img" :srcset="item.images.srcset" alt="dummy" />
          </picture>
          <div class="message">
            <div class="title">{{item.title}}</div>
            {{item.message}}
          </div>
        </div>
      </div>
    </div>
  </v-container>
</template>

<style scoped lang="scss">
.itemsArea{
  padding: 20px;
  background-color: #ededed;
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
    flex-basis: 49%;
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

      .title{
        font-weight: bold;
        font-size: 16px;
      }
    }
  }
  @media screen and (max-width: 900px) {
    .item{
      flex-basis: 100%;
    }
  }

  @media screen and (max-width: 600px) {
    .item{
      flex-basis: 100%;
    }
  }
}

</style>
