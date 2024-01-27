<script setup>
// ref関数を読み込み
import { ref } from 'vue'

 // ref関数に0をセットして定数countに格納
const count = ref(0)

//increment関数を定義
function increment() {
  //定数countの値を+1する
  count.value++
}
</script>

<template>
  <!-- buttonタグの属性にv-on:(省略形は@)を指定 -->
  <!-- 値にincrement関数をセット -->
  <!-- マスタッシュ構文{{}}を用いてref関数の値を動的に展開 -->
  <button @click="increment">count is: {{ count }}</button>
</template>