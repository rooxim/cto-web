<script setup lang="ts">
import webp from "@/assets/dummy.png?preset=img&format=webp&srcset";
import img from "@/assets/dummy.png?preset=img&src";
import srcset from "@/assets/dummy.png?preset=img&srcset";

const items = [
  {
    images: {
      webp,
      img,
      srcset,
    },
    alt: '',
    title: '見積もりによるコストの削減35%',
    text: 'メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ'
  },
  {
    images: {
      webp,
      img,
      srcset,
    },
    alt: '',
    title: '要件、開発のトラッキングによるプロジェクト成功率60%から95%',
    text: 'メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ'
  },
  {
    images: {
      webp,
      img,
      srcset,
    },
    alt: '',
    title: '要件、開発のトラッキングによるプロジェクト成功率60%から95%',
    text: 'メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ メッセージ'
  }
]
</script>
<template>
  <v-container id="advantages">
    <h1>顧問CTOに相談できるメリット</h1>

    <div class="item" v-for="item in items">
      <div>
        <picture>
          <source type="image/webp" :srcset="item.images.webp">
          <img :src="item.images.img" :srcset="item.images.srcset" :alt="item.alt" />
        </picture>
      </div>
      <div>
        <H3 class="commentTitle">{{item.title}}</H3>
        {{item.text}}
      </div>
    </div>
  </v-container>
</template>
<style scoped lang="scss">
#advantages{
  text-align: center;
  img{
    width: 100%;
    max-width: 700px;
    object-fit: contain;
  }

  .item{
    display: flex;
    flex-direction: row;
    margin-top: 20px;
    text-align: left;

    &:nth-child(odd){
      flex-direction: row-reverse;
      text-align: right;
    }

    div{
      padding: 5px;
      &:has(img){
        padding: 0;
        position: relative;
        &:after{
          position: absolute;
          content: '';
          top: 0;
          bottom: 0;
          left: 0;
          right: 0;
          box-shadow: inset 0 0 10px 10px white;
        }
      }

      img{
        position: relative;
        width: 100%;

      }
      flex: 1;
      font-size: 16px;
      .commentTitle{
        font-size: 20px;
        font-weight: bold;
      }
    }
  }

  @media only screen and (max-width: 750px) {
    .item{
      flex-direction: column;
      text-align: left;

      &:nth-child(odd){
        flex-direction: column;
        text-align: left;
      }
    }
  }
}
</style>
