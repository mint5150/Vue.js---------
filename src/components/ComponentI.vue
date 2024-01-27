<script setup>
//ref関数とonMounted関数を読み込み
import { ref, onMounted } from 'vue'

//ref関数にnullをセットして定数pElementRefに格納
const pElementRef = ref(null)

//onMounted関数を定義
onMounted(() => {
  //コンポーネントがマウントされた後に実行される処理
  //定数pElementRefが保持しているDOM要素のテキストコンテンツを'mounted!'に設定
  pElementRef.value.textContent = 'mounted!'
})
</script>

<template>
  <!-- ref属性を使用してpElementRefに参照を格納 -->
  <p ref="pElementRef">hello</p>
</template>