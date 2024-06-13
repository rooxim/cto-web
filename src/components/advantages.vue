<script setup lang="ts">
import webp1 from "@/assets/benefit1.svg";
import img1 from "@/assets/benefit1.svg";
import srcset1 from "@/assets/benefit1.svg";
import webp2 from "@/assets/benefit2.svg";
import img2 from "@/assets/benefit2.svg";
import srcset2 from "@/assets/benefit2.svg";
import webp3 from "@/assets/benefit3.svg";
import img3 from "@/assets/benefit3.svg";
import srcset3 from "@/assets/benefit3.svg";

const items = [
  {
    images: {
      webp:webp1,
      img:img1,
      srcset:srcset1,
    },
    alt: '専門知識に即座にアクセス',
    title: '専門知識に即座にアクセス',
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
    alt: 'プロジェクト成功率の向上',
    title: 'プロジェクト成功率の向上',
    text: '本サービスを利用することで、プロジェクトの成功率が向上に寄与します。従来の相見積りでは、価格競争のために開発業者が無理な工数を提示することがあり、それがプロジェクトの失敗や追加費用の請求につながることがあります。しかし、「あなたの組織のCTO」は最適な業者を選定するアドバイスを提供し、プロジェクトの適切な推進に貢献します。'
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
      line-height: 34px;
      font-size: 18px;
      color: black;

      &:has(picture){
        padding: 0;
      }

      img{
        position: relative;
        width: 100%;

      }
      flex: 1;
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
