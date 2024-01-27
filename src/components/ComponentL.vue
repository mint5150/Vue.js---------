<script setup>
//ref関数を読み込み
import { ref } from 'vue'
//子コンポーネントインポート
import ComponentLChild from './ComponentLChild.vue'

//ref関数に'Hello from parent'をセットして定数greetingに格納
const greeting = ref('Hello from parent')
</script>

<template>
  <!-- 子コンポーネントにプロパティ`msg`として`greeting`を渡す -->
  <ComponentLChild :msg="greeting" />
</template>