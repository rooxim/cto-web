<script setup lang="ts">
import { useField, useForm } from 'vee-validate'
import { required, email, numeric, regex } from '@vee-validate/rules';
import axios from "axios";
import Header from "@/components/header.vue";

const actionURL = 'https://docs.google.com/forms/u/0/d/e/1FAIpQLScOGRJ2pHImasG7ru_oqsbYvt8-RBa6DQFIHDmqXt5PbbqGLg/formResponse';
const survey = [
  {
    name: 'company',
    id: 'entry.1240651423',
    question: '法人名',
    type: 'text',
    label: "法人名",
    placeholder:"法人名",
    validate: (v:string)=>required(v)||'法人名を入力してください。',
    counter: true,
    required: true
  },
  {
    name: 'name',
    id: 'entry.1263330886',
    question: '担当者氏名',
    type: 'text',
    label: '担当者氏名',
    placeholder: '担当者指氏名',
    validate: (v:string)=>required(v)||'担当者指氏名を入力してください。',
    counter: 10,
    required: true
  },
  {
    name: 'nameRead',
    id: 'entry.998885080',
    question: '担当者氏名（カナ）',
    type: 'text',
    label: '担当者氏名（カナ）',
    placeholder: '担当者氏名（カナ）',
    validate: (v:string)=>((required(v) && regex(v,[/^[ァ-ンー]+$/]))||'担当者氏名（カナ）はカタカナで入力してください。'),
    counter: 10,
    required: true
  },
  {
    name: 'phoneNumber',
    id: 'entry.260898957',
    question: '電話番号',
    type: 'text',
    label: '電話番号',
    placeholder: '1234567890',
    validate: (v:string)=>((required(v) && numeric(v)) ||'電話番号はハイフン無しの数字で入力してください。'),
    counter: true,
    required: true
  },
  {
    name: 'email',
    id: 'entry.1801986930',
    question: 'メールアドレス',
    type: 'text',
    label: 'メールアドレス',
    placeholder: 'example@mail.com',
    validate: (v:string)=>((required(v) && email(v)) ||'メールアドレスではありません。メールアドレスを入力してください。'),
    counter: 256,
    required: true
  },
  {
    name: 'message',
    id: 'entry.106675700',
    question: 'お問い合わせ内容',
    type: 'textarea',
    label: 'お問い合わせ内容',
    placeholder: 'お問い合わせ内容',
    validate: (v:string)=>required(v)||'お問い合わせ内容を入力してください。',
    counter: true,
    required: true
  },
];

const schema = new Map();
for (let surveyElement of survey) {
  schema.set(surveyElement.name,(v:string)=>{
    if(!surveyElement.validate)return true;
    const result = surveyElement.validate(v);
    console.log(v, result);
    return result;
  });
}

const {resetForm} = useForm({
  validationSchema: Object.fromEntries(schema)
});
const field = new Map();
for (let surveyElement of survey) {
  field.set(surveyElement.name, useField(surveyElement.name));
}

let submitted = false;

const submit = ()=>{
  submitted = true;
}
const onSubmit = () =>{
  if(submitted){
    alert('お問い合わせありがとうございます。');
    submitted = false;
    resetForm();
  }
}
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
        <form target="hidden_iframe" :action="actionURL" :onsubmit="submit">
        <v-col cols="12" v-for="form in survey">
          <v-text-field v-if="form.type=='text'"
                        v-model="field.get(form.name).value.value"
                        :error-messages="field.get(form.name).errorMessage.value"
                        v-validate="form.validate"
                        variant="outlined"
                        :counter="form.counter"
                        :label="form.label"
                        :placeholder="form.placeholder"
                        :required="form.required"
                        :name="form.id"/>

          <v-textarea v-if="form.type=='textarea'"
                      v-model="field.get(form.name).value.value"
                      :error-messages="field.get(form.name).errorMessage.value"
                      v-validate="form.validate"
                      :counter="form.counter"
                      variant="outlined"
                      :label="form.label"
                      :placeholder="form.placeholder"
                      :required="form.required"
                      :name="form.id" />
        </v-col>
        <v-col cols="12">
          <v-btn type="submit" block color="#dd7c09">お問い合わせ</v-btn>
        </v-col>
        </form>
        <iframe name="hidden_iframe" style="display: none" :onload="onSubmit"></iframe>
      </v-row>
    </v-container>
  </v-app>
</template>

<style scoped lang="scss">
.container{
  margin-right: auto;
  margin-left: auto;
  min-width: 320px;
  max-width: 500px;
  width: 100%;
  form{
    width: 100%;
  }
}
</style>
