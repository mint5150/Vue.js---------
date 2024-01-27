<script setup>
// ref関数を読み込み
import { ref } from 'vue'

 // ref関数に''をセットして定数textに格納
const text = ref('')

//onInput関数を定義、引数にe（イベントオブジェクト）をセット
//v-modelの場合はonInput関数は不要
function onInput(e) {
  //inputイベントが発生したときの入力フィールドの値＝入力された値を定数テキストの値として代入する
  text.value = e.target.value
}
</script>

<template>
  <!-- h1タグの属性にv-bind:(省略形は:)を指定 -->
  <!-- inputタグのvalue属性を変数textの値としてバインドする -->
  <!-- h1タグの属性にv-on:(省略形は@)を指定 -->
  <!-- inputイベントが発生する度にonInput関数が入力フィールドで呼ばれる -->
  <input :value="text" @input="onInput" placeholder="Type here">

  <!-- h1タグの属性にv-modelを指定 -->
  <!-- v-model は <input> の値をバインドされた状態と自動的に同期する -->
  <input v-model="text" placeholder="Type here">
  <!-- マスタッシュ構文{{}}を用いて定数textの値を動的に展開 -->
  <p>{{ text }}</p>
</template>