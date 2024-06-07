<script setup lang="ts">

import Header from "@/components/header.vue";
</script>
<template>
  <v-app>
    <Header />
    <h1>お問い合わせ</h1>
    <v-container class="container">
      <v-row align="center">
        <v-col cols="12">
          <div>
            弊社にご興味をお持ちいただきまして、ありがとうございます。<br>
            以下よりお問い合わせください。
          </div>
        </v-col>
      </v-row>
      <v-row align="center">
        <v-col cols="12">
          <v-text-field
              variant="outlined"
              :counter="10"
              label="法人名"
              placeholder="法人名"
              required />
        </v-col>
        <v-col cols="12">
          <v-text-field
              variant="outlined"
              :counter="10"
              label="担当者指氏名"
              placeholder="担当者指氏名"
              required />
        </v-col>
        <v-col cols="12">
          <v-text-field
              variant="outlined"
              :counter="10"
              label="担当者指氏名(カナ)"
              placeholder="担当者指氏名(カナ)"
              required />
        </v-col>
        <v-col cols="12">
          <v-text-field
              variant="outlined"
              :counter="12"
              label="電話番号"
              placeholder="1234567890"
              required />
        </v-col>
        <v-col cols="12">
          <v-text-field
              variant="outlined"
              :counter="true"
              label="メールアドレス"
              placeholder="example@mail.com"
              required />
        </v-col>
        <v-col cols="12">
          <v-textarea
              variant="outlined"
              label="お問い合わせ内容">

          </v-textarea>
        </v-col>
        <v-col cols="12">
          <v-btn block color="#dd7c09">お問い合わせ</v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<style scoped lang="scss">
.container{
  min-width: 320px;
  max-width: 500px;
  width: 100%;
}
</style>
