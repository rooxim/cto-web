<template>
  <v-container fluid class="main">
    <div class="content">
      <div class="message">
        あなたの組織のCTO
      </div>
      <div class="subMessage">必要な時間だけ、必要なタイミングで</div>

      <div class="key-area">
        <div class="key">1位. CTOがほしい</div>
        <div class="key">2位. 費用を抑えたい</div>
        <div class="key">3位. 技術的意見がほしい</div>
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
}
.key{
  padding: 10px;
  //background-image: linear-gradient(to right, red , #dd7c09);
  //border-radius: 100px;
  font-weight: bold;
  //color: white;
  text-align: center;
  font-size: 14px;
  border-bottom: solid 1px;
}
</style>
<script setup lang="ts">
</script>
