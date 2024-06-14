<template>
  <v-container fluid class="main">
    <div class="content">
      <div class="message">
        あなたの組織のCTO
      </div>
      <div class="subMessage">定額の顧問CTOサービス</div>

      <div class="key-area">
        <div class="title">よくあるお悩み</div>
        <div class="key">1位. 技術的な意見がほしい</div>
        <div class="key">2位. 無駄な開発費用をを抑えたい</div>
        <div class="key">3位. 会社に技術経営の要観点入れたい</div>
      </div>
    </div>
  </v-container>
</template>

<style scoped lang="scss">
.main{
  height: 500px;
  background-image: url("@/assets/main.jpg?preset=img&src");
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: start;

  padding: 0;
  position: relative;
  &:after{
    position: absolute;
    content: '';
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    //box-shadow: inset 0 -20px 15px -15px white;
  }
}
.content{
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: center;
  padding-left: 40px;
  background-color: rgba(255, 255, 255, 0.31);
  box-shadow: 0px 0px 10px 10px rgba(255, 255, 255, 0.31);
}
.message{
  font-weight: bold;
  font-size: 30px;
}
.key-area{
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: space-around;
  width: 25em;

  .title{
    font-weight: bold;
    font-size: 18px;
  }

  .key{
    margin-top: 10px;
    padding: 5px;
    font-weight: bold;
    text-align: center;
    font-size: 18px;
    line-height: 18px;
    border-bottom: solid 1px red;
    color: black;
    border-radius: 5px;
    background-color: rgb(255, 221, 221);
  }
}

</style>
<script setup lang="ts">
</script>
