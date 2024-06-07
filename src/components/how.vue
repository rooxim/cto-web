<script setup lang="ts">


</script>
<template>
  <v-container id="how">
    <h1>サービスのご紹介</h1>
    <div class="message">
      Slack、Line、Chatworksにてご質問頂けます。<br>
      まずは御社のSlack、Line、Chatworksに弊社アカウントを追加いただきます。<br>
      あとは、ご質問いただければ技術的な質問にご回答させていただきます！
    </div>

    <h2>導入までの流れ</h2>
    <div class="step">
      <div class="action">お申し込み(お支払い)</div>
      <span class="dli-arrow-down"></span>
      <div class="action">弊社よりご連絡<br>(ツールの設定のご依頼)</div>
      <span class="dli-arrow-down"></span>
      <div class="action">ツールに弊社アカウントを追加いただく</div>
      <span class="dli-arrow-down"></span>
      <div class="action">ご質問があるときにメッセージを送るだけ</div>
    </div>
    <div class="notion">
      <p>※ 導入までに最大3営業日要する可能性があります。</p>
    </div>


    <h2>チケットについて</h2>

    <div class="message">
    チケットを事前に購入いただくことで、資料やお見積りの作成などお時間の掛かる作業をご依頼していただくことが出来ます。
    </div>
    <div class="step">
      <div class="action">チケットをご購入</div>
      <span class="dli-arrow-down"></span>
      <div class="action">弊社から作業に必要な<br>お時間をご提示させていただきます。</div>
      <span class="dli-arrow-down"></span>
      <div class="action">ご依頼をお申し付けください</div>
      <span class="dli-arrow-down"></span>
      <div class="action">弊社にて作業を開始</div>
    </div>

  </v-container>
</template>
<style scoped lang="scss">
#how{
  .notion, .message{
    max-width: 50%;
    margin-top: 20px;
    width: 50%;
    margin-left: auto;
    margin-right: auto;
  }

  .step{
    text-align: center;
  }

  .action{
    width: 50%;
    margin-left: auto;
    margin-right: auto;
    background-color: #dd7c09;
    border-radius: 100px;
    color: white;
    padding: 20px;
    text-align: center;
    font-weight: bold;
  }
}
</style>
