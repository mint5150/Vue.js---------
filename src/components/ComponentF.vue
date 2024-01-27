<script setup>
// ref関数を読み込み
import { ref } from 'vue'

 // ref関数にtrueをセットして定数awsomeに格納
const awesome = ref(true)

//toggle関数を定義
function toggle() {
  //定数awesomeの値にカレントと反対の値を代入
  awesome.value = !awesome.value
}
</script>

<template>
  <!-- buttonタグの属性にv-on:(省略形は@)を指定 -->
  <!-- クリックイベントが発生する度にtoggle関数が呼ばれる -->
  <button @click="toggle">toggle</button>
  <!-- h1タグの属性にv-ifを指定 -->
  <!-- 値に定数awsomeの値（true or false）をセット -->
  <!-- trueになった方だけが表示される -->
  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>
</template>