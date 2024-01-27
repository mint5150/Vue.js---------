<script setup>
//ref関数を読み込み
import { ref } from 'vue'
//子コンポーネントを読み込み
import ComponentMChild from './ComponentMChild.vue'

//ref関数に'No child msg yet'をセットして定数childMsgに格納
const childMsg = ref('No child msg yet')
</script>

<template>
  <!-- 子コンポーネントをテンプレート内で使用する -->
  <!-- responseイベントが発生したときにchildMsgにメッセージをセット -->
  <ComponentMChild @response="(msg) => childMsg = msg" />
  <!-- マスタッシュ構文{{}}を用いてchildMsgのテキストの値を動的に展開 -->
  <p>{{ childMsg }}</p>
</template>