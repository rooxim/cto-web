<script setup lang="ts">

</script>
<template>
  <v-container id="prices">
    <h1>プラン</h1>

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
