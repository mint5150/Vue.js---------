<script setup>
//defineEmitsを使用してresponseイベントを宣言し定数emitに格納する
const emit = defineEmits(['response'])

//イベントを発火して親コンポーネントにメッセージを送信
emit('response', 'hello from child')
</script>

<template>
  <h2>Child component</h2>
</template>