<script setup lang="ts">

const plans = [
  {
    name: 'スタンダードプラン',
    consultation: '相談し放題',
    ticket: '0枚/月',
    priceMonth: '9,800円/月',
    priceYear: '100,000円/月',
    setupCost: '4,900円',
    color: '#ececec'
  },
  {
    name: 'プレミアムプラン',
    consultation: '相談し放題',
    ticket: '1枚/月',
    priceMonth: '24,800円/月',
    priceYear: '248,000円/月',
    setupCost: '4,900円',
    color: '#b3ea96'
  },
  {
    name: 'プラチナプラン',
    consultation: '相談し放題',
    ticket: '10枚/月',
    priceMonth: '198,000円/月',
    priceYear: '1,980,000円/月',
    setupCost: '0円',
    color: '#c6eeff'
  }
];

const displayItems = [
  {key: 'consultation' , name: "相談"},
  {key: 'ticket' , name: "チケット"},
  {key: 'priceMonth' , name: "月々支払い"},
  {key: 'priceYear' , name: "年一括支払い"},
  {key: 'setupCost', name: "初回手数料"}
];
</script>
<template>
  <v-container id="prices">
    <h1>料金プラン</h1>

    <table class="price-table">
      <thead>
      <tr>
        <td></td>
        <td v-for="item in plans" :style="{'--border-color':item.color}">
          <div class="head">{{item.name}}</div>
        </td>
      </tr>
      </thead>
      <tbody>
      <tr v-for="displayItem in displayItems">
        <td>{{displayItem.name}}</td>
        <td v-for="item in plans"  :style="{'--border-color':item.color}">
          <div class="item">{{ item[displayItem.key] }}</div>
        </td>
      </tr>
      </tbody>
    </table>

    <h2>チケット</h2>
    <div>
      ご相談では、メッセージによるご回答がメインとなります。<br>
      しかし、ご相談だけでは資料による提示や、見積もりを要するご回答などは出来ません。<br>
      そこでご相談とは別にチケットを消費することによって時間を要する作業をご依頼して頂けます。<br>

      チケット１枚でおよそ4時間分の資料や見積もり作成を依頼頂けます。<br>
      チケットは発行から1年で期限が切れる形となります。<br>
      1チケット: 20,000円で追加購入頂けます。<br>
    </div>

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
        border-left: solid 1px var(--border-color);
        border-right: solid 1px var(--border-color);
      }

      tr:last-child{
        td{
          border-bottom: solid 1px var(--border-color);
          border-radius: 0 0 10px 10px;
        }
        td:first-child{
          border-bottom: none;
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
