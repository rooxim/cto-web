<script setup lang="ts">

const plans = [
  {
    name: 'スタンダードプラン',
    consultation: '相談し放題',
    ticket: '技術相談',
    priceMonth: '9,800円/月',
    priceYear: '100,000円/月',
    setupCost: '4,900円',
    color: '#ececec',
    payment: 'https://buy.stripe.com/test_6oEcOzdMO4Kr8V27su',
  },
  {
    name: 'プレミアムプラン',
    consultation: '相談し放題',
    ticket: '技術相談 / 工数見積り / 最適化検討 / その他懸念事項相談',
    priceMonth: '24,800円/月',
    priceYear: '248,000円/月',
    setupCost: '4,900円',
    color: '#b3ea96',
    payment: 'https://buy.stripe.com/test_9AQ01N246ccT2wEdQR'
  },
  // {
  //   name: 'プラチナプラン',
  //   consultation: '相談し放題',
  //   ticket: '10枚/月',
  //   priceMonth: '198,000円/月',
  //   priceYear: '1,980,000円/月',
  //   setupCost: '0円',
  //   color: '#c6eeff'
  // }
];

const displayItems = [
  // {key: 'consultation' , name: "相談"},
  {key: 'ticket' , name: "対応内容"},
  {key: 'priceMonth' , name: "月々支払い"},
  {key: 'priceYear' , name: "年一括支払い"},
  // {key: 'setupCost', name: "初回手数料"}
];
</script>
<template>
  <v-container id="prices">
    <h1>プラン</h1>

<!--    <table class="price-table">-->
<!--      <thead>-->
<!--      <tr>-->
<!--        <td></td>-->
<!--        <td v-for="item in plans" :style="{'&#45;&#45;border-color':item.color}">-->
<!--          <div class="head">{{item.name}}</div>-->
<!--        </td>-->
<!--      </tr>-->
<!--      </thead>-->
<!--      <tbody>-->
<!--      <tr v-for="displayItem in displayItems">-->
<!--        <td>{{displayItem.name}}</td>-->
<!--        <td v-for="item in plans"  :style="{'&#45;&#45;border-color':item.color}">-->
<!--          <div class="item">{{ item[displayItem.key] }}</div>-->
<!--        </td>-->
<!--      </tr>-->
<!--      <tr>-->
<!--        <td></td>-->
<!--        <td v-for="item in plans"  :style="{'&#45;&#45;border-color':item.color}">-->
<!--          <div class="item"><v-btn size="x-large" :href="item.payment" :color="item.color" block>{{item.name}}に申し込む</v-btn></div>-->
<!--        </td>-->
<!--      </tr>-->
<!--      </tbody>-->
<!--    </table>-->


    <stripe-pricing-table pricing-table-id="prctbl_1PP2LIBcykgBJMyJ30UuNymf"
                          publishable-key="pk_test_51KtqDVBcykgBJMyJBEMfGm2vma6X2RS3hqQ5vmbHG97UpvjCzSL8yy75wg8XdFDbWeg8uJhnSGfIpcGm9r0M4NuO00OVoqRmgu">
    </stripe-pricing-table>

<!--    技術相談-->
<!--    こんな質問と解答が出来てます。-->

<!--    工数見積り-->
<!--    アイミツを取ったけど、-->
<!--    安く見積もったばかりに、プロジェクトが失敗した。-->
<!--    安物買いの銭失い的な絵-->


<!--    事例と解決案を提示する。-->
  </v-container>
</template>
<style scoped lang="scss">
#prices{
  text-align: center;

  table{
    border-spacing: 20px 0;
    margin-top: 40px;
    margin-left: auto;
    margin-right: auto;

    --border-color: #ececec;

    thead{

      td{
        border-left: solid 1px var(--border-color);
        border-right: solid 1px var(--border-color);
        border-radius: 10px 10px 0 0;

        .head{
          border-radius: 10px;
          background-color: var(--border-color);
          padding: 10px 30px;
        }
      }
      td:first-child{
        border-left: none;
        border-right: none;
      }
    }

    tbody{
      tr{
        padding: 0;
        margin: 0;
      }

      td{
        height: 45px;
        padding: 0 10px;
        border-left: solid 1px var(--border-color);
        border-right: solid 1px var(--border-color);
      }

      tr:nth-last-child(2){
        td{
          border-bottom: solid 1px var(--border-color);
          border-radius: 0 0 10px 10px;
        }
        td:first-child{
          border-bottom: none;
        }
      }

      tr:last-child {
        td{
          padding: 10px;
          border: none;
        }
      }
      td:first-child{
        text-align: right;
        border-left: none;
        border-right: none;
      }
    }
  }
}
</style>
