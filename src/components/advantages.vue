<script setup lang="ts">
import webp1 from "@/assets/benefit1.svg?preset=img&format=svg&srcset";
import img1 from "@/assets/benefit1.svg?preset=img&format=svg&src";
import srcset1 from "@/assets/benefit1.svg?preset=img&format=svg&srcset";
import webp2 from "@/assets/benefit2.svg?preset=img&format=webp&srcset";
import img2 from "@/assets/benefit2.svg?preset=img&format=svg&src";
import srcset2 from "@/assets/benefit2.svg?preset=img&format=svg&srcset";
import webp3 from "@/assets/benefit3.svg?preset=img&format=webp&srcset";
import img3 from "@/assets/benefit3.svg?preset=img&format=svg&src";
import srcset3 from "@/assets/benefit3.svg?preset=img&format=svg&srcset";

const items = [
  {
    images: {
      webp:webp1,
      img:img1,
      srcset:srcset1,
    },
    alt: '即座の専門知識へのアクセス',
    title: '即座の専門知識へのアクセス',
    text: 'システム開発に関する質問が発生した際に、専門家の意見や助言を直ちに得ることができます。これにより、プロジェクトの進行がスムーズになり、問題解決にかかる時間が短縮されます。'
  },
  {
    images: {
      webp:webp2,
      img:img2,
      srcset:srcset2,
    },
    alt: 'リソースの柔軟な利用',
    title: 'リソースの柔軟な利用',
    text: 'プロジェクトに必要なプロフェッショナルな意見やアドバイスを必要な時に必要なだけ利用できるため、リソースの効率的な活用が可能です。組織内に特定の専門家を雇う必要がなくなり、プロジェクトのニーズに応じて柔軟に対応できます。\n' +
        '\n'
  },
  {
    images: {
      webp:webp3,
      img:img3,
      srcset:srcset3,
    },
    alt: '効率的な資源活用',
    title: '効率的な資源活用',
    text: '定額制のサービスとして提供されるため、予算を管理しやすくなります。従来のコンサルティングサービスに比べて予測可能性が高く、予想外の費用が発生するリスクを軽減します。'
  }
]
</script>
<template>
  <v-container id="advantages">
    <h1>サービスの特徴</h1>

    <div class="item" v-for="item in items">
      <div>
        <picture>
<!--          <source type="image/webp" :srcset="item.images.webp">-->
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
    margin-top: 40px;
    text-align: left;

    &:nth-child(even){
      flex-direction: row-reverse;
      text-align: left;
    }

    div{
      padding: 20px 40px;

      &:has(picture){
        padding: 0;
      }

      img{
        position: relative;
        width: 100%;

      }
      flex: 1;
      font-size: 16px;
      .commentTitle{
        color: #dd7c09;
        font-size: 24px;
        font-weight: bold;
      }
    }
  }

  @media only screen and (max-width: 750px) {
    .item{
      flex-direction: column;

      &:nth-child(even){
        flex-direction: column;
      }
    }
  }
}
</style>
