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

import webpHm4 from "@/assets/hm4.jpg?preset=img&format=webp&srcset";
import imgHm4 from "@/assets/hm4.jpg?preset=img&src";
import srcsetHm4 from "@/assets/hm4.jpg?preset=img&srcset";

import webpHm5 from "@/assets/hm5.jpg?preset=img&format=webp&srcset";
import imgHm5 from "@/assets/hm5.jpg?preset=img&src";
import srcsetHm5 from "@/assets/hm5.jpg?preset=img&srcset";
const items = [
  {
    images:{
      webp:webpHm4,
      img:imgHm4,
      srcset:srcsetHm4,
    },
    title: 'アイデアの実現性を検証したいがわからない',
    message: '「あなたの組織のCTO」では、あなたのアイデアの実現性を技術的観点からの検証にご利用頂けます。\n' +
        '適切な技術スタックやアーキテクチャの選定、スケーラビリティやセキュリティの確認などを行い、プロトタイプ開発に向けた詳細な計画を提供します。\n' +
        'これにより、<span>リスクを最小限に抑えた実装が可能</span>となります。'
  },
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
    title: '新規事業を始めるがなにをしたら良いかわからない',
    message: '「あなたの組織のCTO」は、新規事業の立ち上げにおける専門知識と経験を提供します。\n' +
        'ビジネスアイデアの技術的実現可能性や市場適合性を評価し、具体的な実行計画を策定する支援を行います。\n' +
        'これにより、プロジェクトの立ち上げがスムーズに進み、<span>効率的なリソース活用</span>が実現します。'
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
  },
  {
    images:{
      webp:webpHm5,
      img:imgHm5,
      srcset:srcsetHm5,
    },
    title: '妥当性を技術観点からの検証したいがわからない',
    message: '「あなたの組織のCTO」は、技術的な妥当性を徹底的に検証するための専門知識を提供します。\n' +
        'アーキテクチャの適合性、技術的な挑戦に対するソリューションの提案、および開発プロセスにおける最善の実践を指導します。\n' +
        'これにより、<span>プロジェクトの長期的な成功と成長をサポート</span>します。'
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
