<script setup>
//ref関数を読み込み
import { ref } from 'vue'
//子コンポーネントを読み込み
import ComponentNChild from './ComponentNChild.vue'

//ref関数に'from parent'をセットして定数msgに格納
const msg = ref('from parent')
</script>

<template>
  <!--子コンポーネントを呼び出し  -->
  <!--スロットを使用して親コンポーネントのメッセージを挿入-->
  <ComponentNChild>Message: {{ msg }}</ComponentNChild>
</template>