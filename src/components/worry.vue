<script setup lang="ts">
import webp from "@/assets/dummy.png?preset=img&format=webp&srcset";
import img from "@/assets/dummy.png?preset=img&src";
import srcset from "@/assets/dummy.png?preset=img&srcset";

import webpHm1 from "@/assets/hm1.jpg?preset=img&format=webp&srcset";
import imgHm1 from "@/assets/hm1.jpg?preset=img&src";
import srcsetHm1 from "@/assets/hm1.jpg?preset=img&srcset";

import webpHm2 from "@/assets/hm2.jpg?preset=img&format=webp&srcset";
import imgHm2 from "@/assets/hm2.jpg?preset=img&src";
import srcsetHm2 from "@/assets/hm2.jpg?preset=img&srcset";

import webpMoni from "@/assets/moni.jpg?preset=img&format=webp&srcset";
import imgMoni from "@/assets/moni.jpg?preset=img&src";
import srcsetMoni from "@/assets/moni.jpg?preset=img&srcset";

import webpHm3 from "@/assets/hm3.jpg?preset=img&format=webp&srcset";
import imgHm3 from "@/assets/hm3.jpg?preset=img&src";
import srcsetHm3 from "@/assets/hm3.jpg?preset=img&srcset";
const items = [
  {
    images:{
      webp:webpHm1,
      img:imgHm1,
      srcset:srcsetHm1,
    },
    title: '相見積りでコストを抑えて開発をしたけれど、プロジェクトが失敗した。',
    message: '相見積りでは受託側業者は価格競争で勝つために無理な開発工数の算出で契約を取ろうとする場合が少なくともありません。\n' +
        '実際に<span>作りたかったシステムにならない</span>又は開発途中で<span>追加の費用を請求される</span>事例が多々あります。' +
        '本サービスでは最適な業者を選定判断を行うアドバイスを行います。\n' +
        '結果、プロジェクトの成功率向上に寄与します。'
  },{
    images:{
      webp:webpHm2,
      img:imgHm2,
      srcset:srcsetHm2,
    },
    title: 'システムの開発を依頼したいけど、納品までの対応、流れがわからない。',
    message: '「システム開発業者に依頼して開発をすすめてもらっておけばいいのでは」と思うでしょうがそれは危険です。' +
        '受託側のゴールは委託者に納品することですが、委託者は完成物を運用していく事も考えなければなりません。\n' +
        'しかし、委託者の技術知識の有無によっては運用も完全委託となり<span>想定コストが増加する</span>傾向にあります。' +
        'これを防ぐため、本サービスでは、お客様の技術知識のサポートをさせていただきます。'
  },
  {
    images:{
      webp: webpMoni,
      img: imgMoni,
      srcset: srcsetMoni,
    },
    title: 'エンジニアに開発をお願いしているが専門用語が多く理解に苦しむ',
    message: 'エンジニアは専門用語を利用した会話をしがちです。\n' +
        '本サービスはエンジニアの話している内容をわかりやすく要約してお伝えさせていただきます。\n' +
        'これにより委託者、<span>受託者とのコミュニケーションが円滑になる</span>事により、より良いプロジェクト進行に寄与します。'
  },
  {
    images:{
      webp:webpHm3,
      img:imgHm3,
      srcset:srcsetHm3,
    },
    title: '技術選定をしたが、問題がないかチェックする機構がない',
    message: '本サービスではプロジェクトに必要な技術選定からご相談いただけます。\n' +
        '最適な技術に基づく、<span>効率的な開発</span>を進めることが可能です。'
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
            <div v-html="item.message"></div>
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
      object-fit: cover;
    }

    .message{
      padding: 0 5px;
      font-size: 18px;
      line-height: 30px;

      .title{
        font-weight: bold;
        font-size: 20px;
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
<style  lang="scss">
#worry{
  .message{
    span{
      font-weight: bold;
      color: red;
    }
  }
}
</style>
