<script setup>
//ref関数とwatch関数を読み込み
import { ref, watch } from 'vue'

//ref関数に1をセットして定数todoIdに格納
const todoId = ref(1)
//ref関数にnullをセットして定数todoDataに格納
const todoData = ref(null)

//非同期関数fetchDataを定義
async function fetchData() {
  //定数todoDataの値をnullに設定（初期化）
  todoData.value = null
  //JSONPlaceholderからtodoデータを取得して定数resに格納
  const res = await fetch(
    `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
  )
  //取得したデータを定数todoDataの値として設定
  todoData.value = await res.json()
}

//コンポーネントがマウントされた際に初回データを取得
fetchData()

//todoIdの変更を監視して、変更があればfetchDataを再実行
watch(todoId, fetchData)
</script>

<template>
  <!-- マスタッシュ構文{{}}を用いてTodoのIDの値を動的に展開 -->
  <p>Todo id: {{ todoId }}</p>
  <!-- 三項演算子を用いてボタンをクリックするとtodoIdを増やし、次のTodoを取得 -->
  <!-- !todoDataがtrueの場合はボタンが無効になる -->
  <button @click="todoId++" :disabled="!todoData">Fetch next todo</button>
  <!-- todoDataがnullの場合は"Loading..."を表示 -->
  <p v-if="!todoData">Loading...</p>
  <!-- todoDataが存在する場合はマスタッシュ構文{{}}を用いて定数todoDataのIDの値を動的に展開 -->
  <pre v-else>{{ todoData }}</pre>
</template>