<script setup lang="ts">

</script>

<template>
  <div id="access">
    <h1>アクセス</h1>
    <div class="main">
      <div>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1620.9415984146292!2d139.69371253967284!3d35.65524930000001!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60188b55ca5c890d%3A0x8fca34104c657664!2z5Y2X5bmz5Y-w77yR77yV77yR77yQ44OT44Or!5e0!3m2!1sja!2sus!4v1716883512472!5m2!1sja!2sus" width="100%" height="250" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
      <div>
        <div class="name">ROOXIM株式会社</div>
        <table>
          <tr>
            <td>郵便番号:</td>
            <td>〒150-0036</td>
          </tr>
          <tr>
            <td>住所:</td>
            <td>東京都渋谷区南平台町15-10 プチビル2F</td>
          </tr>
          <tr>
            <td>電話番号:</td>
            <td>+81 (0)50-3136-6541</td>
          </tr>
        </table>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
#access{
  margin-top: 20px;
  .title{
    text-align: center;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 10px;
  }
  .main{
    display: flex;
    >div{
      flex: 1;
    }

    .name{
      font-weight: bold;
      font-size: 20px;
    }

    div:last-child{
      padding-left: 10px;
    }

    table{
      font-size: 18px;
      td:first-child{
        width: 150px;
      }
    }
  }

  @media only screen and (max-width: 750px) {
    .main{
      flex-direction: column;

      table{
        font-size: 20px;
      }
    }
  }
}
</style>
