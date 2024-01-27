<script setup>
// ref()とreactive()を両方読み込み
import { ref, reactive } from 'vue'

// ref関数に値を定義して定数messageに格納
const message = ref('Hello World!')

// reactive関数に値を定義して定数counterに格納
const counter = reactive({ count: 1 })
</script>

<template>
  <!-- マスタッシュ構文{{}}を用いてref関数の値を動的に展開 -->
  <h1>{{ message }}</h1>

  <!-- マスタッシュ構文{{}}を用いてreactive関数の値を動的に展開 -->
  <p>Count is: {{ counter.count }}</p>
</template>