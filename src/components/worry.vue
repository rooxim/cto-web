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
    message: '相見積りでは受託側業者はミニマムで見積もって安く見せてきます。' +
        '結果、実際に作りたかったシステムとならないことや、管理に予想以上の費用がかかってしまうなどの問題が発生します。' +
        'このサービスでは相見積りの結果から最適な業者を選ぶお手伝いをさせていただきます。' +
        'もしくは工数を算出させて頂き、より正確な過不足のない見積もりをださせていただくことも可能です。' +
        '過不足のない見積もりにすることで、プロジェクトの成功率向上に寄与します。'
  },{
    images:{
      webp:webpHm2,
      img:imgHm2,
      srcset:srcsetHm2,
    },
    title: 'システムの開発を依頼したいけどなにをしたらいいかわからない。',
    message: '「システム開発業者に依頼して開発をすすめてもらっておけばいいのでは？」と思うでしょうがそれは間違いです。' +
        'システムの開発は委託側と受託側で一緒になって作るものです。' +
        '受託側のゴールは委託者に納品することですが、委託者はそれを運用していくことが求められます。' +
        'この際、委託者がシステム開発で関わっていないと、急に運用なんて出来ないのです。' +
        'したがって、システム開発は運用を考えて、委託者、受託者が一緒になって開発していくべきです。' +
        'しかし、委託者には開発に関わるのは、知識的に難しいと思います。' +
        'このサービスでは、あなたの知識のサポートさせていただきます。'
  },
  {
    images:{
      webp: webpMoni,
      img: imgMoni,
      srcset: srcsetMoni,
    },
    title: 'エンジニアに開発をお願いしているが何を言っているかわからない。',
    message: 'エンジニアは、専門的な会話をしがちです。' +
        '専門的な会話でわからないというさいにあなたの組織のCTOにご相談ください。' +
        'エンジニアの話している内容をわかりやすく要約してお伝えさせていただきます。' +
        'これにより委託者、受託者のコミュニケーションが円滑になってより良い開発に寄与します。'
  },
  {
    images:{
      webp:webpHm3,
      img:imgHm3,
      srcset:srcsetHm3,
    },
    title: '技術選定をしたが、本当に問題ないか不安',
    message: 'あなたの組織のCTOでは、プロジェクトの技術選定からご相談いただけます。' +
        'ご相談の結果をCTOと確認しながら開発を進めることで、自信を持って開発を進めることが可能です。'
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
      object-fit: cover;
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
