<script setup lang="ts">

</script>
<template>
  <v-container id="prices">

    <h1>プラン</h1>

    <div class="red">
      年額だと2ヶ月分無料
    </div>

    <stripe-pricing-table pricing-table-id="prctbl_1PP2LIBcykgBJMyJ30UuNymf"
                          publishable-key="pk_test_51KtqDVBcykgBJMyJBEMfGm2vma6X2RS3hqQ5vmbHG97UpvjCzSL8yy75wg8XdFDbWeg8uJhnSGfIpcGm9r0M4NuO00OVoqRmgu">
    </stripe-pricing-table>


    スタンダード　9800円
    プレミアム　528000円


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
  .red{
    color: red;
    font-weight: bold;
    font-size: 25px;
  }

  .emphasis {
    font-weight: bold;
    font-size: 20px;
  }
}
</style>
