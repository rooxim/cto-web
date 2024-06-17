<script setup lang="ts">

</script>
<template>
  <v-container id="prices">

    <h1>プラン</h1>

    <div class="notion">
      年額だと2ヶ月分無料
    </div>

    <stripe-pricing-table pricing-table-id="prctbl_1PRXibBcykgBJMyJb0dY7CSz"
                          publishable-key="pk_live_51KtqDVBcykgBJMyJjFFzdgAsejY0oFCPtpENBuXsuC62jj6gMStbltWuj9TTPhK7V21tOTeEmSwQ77zpNFCkmsLp00nmpF1Y6A">
    </stripe-pricing-table>

    <div>
      ※技術作業工数が発生する場合は、別途お見積りが必要な場合があります。
    </div>

    <div class="note">
      <p><span class="emphasis">スタンダードプランプラン</span>は、<span class="emphasis">フリーランス</span>や<span class="emphasis">個人事業主</span>の方におすすめのプランです。</p>
      <p><span class="emphasis">プレミアムプラン</span>は、<span class="emphasis">その他法人</span>の方におすすめのプランです。</p>
    </div>
  </v-container>
</template>
<style scoped lang="scss">
#prices{
  text-align: center;

  .note{
    margin-top: 20px;
    font-size: 24px;
  }
  .notion{
    color: red;
    font-weight: bold;
    font-size: 25px;
    line-height: 80px;
  }

  .emphasis {
    font-weight: bold;
    font-size: 20px;
  }
}
</style>
