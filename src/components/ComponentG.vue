<script setup>
// ref関数を読み込み
import { ref } from 'vue'

//変数idに0をセット
let id = 0

//ref関数に''をセットして定数newTodoに格納
const newTodo = ref('')
//ref関数に中身がオブジェクトの配列をセットして定数Todosに格納
//id: id++の式で現在のidの値を使用してオブジェクトにidプロパティを設定し、その後にidを1増やすことで、各Todoオブジェクトのidは一意に連続的に増加する
const todos = ref([
  { id: id++, text: 'Learn HTML' },
  { id: id++, text: 'Learn JavaScript' },
  { id: id++, text: 'Learn Vue' }
])

//addTodo関数を定義
function addTodo() {
  //todos.valueの末尾に新しいTodoオブジェクトを追加
  todos.value.push({ id: id++, text: newTodo.value })
  //newTodoの値をリセット
  newTodo.value = ''
}

//removeTodo関数を定義
function removeTodo(todo) {
  //todos.valueから指定されたtodoオブジェクトをフィルタリングして削除
  todos.value = todos.value.filter((t) => t !== todo)
}
</script>

<template>
  <!-- フォームのsubmitイベントを検知し、addTodo関数を実行 -->
  <form @submit.prevent="addTodo">
    <!-- newTodoの双方向バインディング -->
    <input v-model="newTodo">
    <button>Add Todo</button>
  </form>
  <ul>
    <!-- todosの各要素に対して繰り返し処理し結果を変数todoに代入する -->
    <li v-for="todo in todos" :key="todo.id">
      <!-- マスタッシュ構文{{}}を用いてtodoのテキストの値を動的に展開 -->
      {{ todo.text }}
      <!-- ボタンがクリックされたときにremoveTodo関数を実行 -->
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>

<style>
  ul {
    list-style-type: none;
  }
</style>