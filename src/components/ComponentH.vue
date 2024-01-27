<script setup>
// ref関数とcomputed関数を読み込み
import { ref, computed } from 'vue'

//変数idに0をセット
let id = 0

//ref関数に''をセットして定数newTodoに格納
const newTodo = ref('')

//ref関数にfalseをセットして定数hideCompletedに格納
//（完了したtodoを非表示にするかどうかを管理するリアクティブ変数）
const hideCompleted = ref(false)

//ref関数に中身がオブジェクトの配列をセットして定数Todosに格納
//id: id++の式で現在のidの値を使用してオブジェクトにidプロパティを設定し、その後にidを1増やすことで、各Todoオブジェクトのidは一意に連続的に増加する
const todos = ref([
  { id: id++, text: 'Learn HTML', done: true },
  { id: id++, text: 'Learn JavaScript', done: true },
  { id: id++, text: 'Learn Vue', done: false }
])

//Vueのcomputed関数を使用して、計算されたプロパティを作成
//定数filteredTodosに格納する
//三項演算子を用いてhideCompletedの値を条件として確認
//hideCompletedがtrueの場合は、未完了のtodoのみをフィルタリング
//hideCompletedがfalseの場合は、すべてのtodoをそのまま返す
const filteredTodos = computed(() => {
  return hideCompleted.value
    ? todos.value.filter((t) => !t.done)
    : todos.value
})

//addTodo関数を定義
function addTodo() {
  //todos.valueの末尾に新しいTodoオブジェクトを追加
  todos.value.push({ id: id++, text: newTodo.value, done: false })
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
    <li v-for="todo in filteredTodos" :key="todo.id">
      <!-- Todoの完了状態を制御するためのチェックボックス -->
      <input type="checkbox" v-model="todo.done">
      <!-- 完了したTodoにはline-throughスタイルを適用 -->
      <!-- マスタッシュ構文{{}}を用いてtodoのテキストの値を動的に展開 -->
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
      <!-- ボタンがクリックされたときにremoveTodo関数を実行 -->
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
  <!-- 完了したtodoを非表示にするかどうかを切り替えるボタン -->
  <!-- ボタンがクリックされた時にhideCompletedの値を反転させる -->
  <button @click="hideCompleted = !hideCompleted">
    <!-- hideCompletedの値に応じてボタンのラベルを動的に変更 -->
    <!-- 三項演算子を使用して、hideCompletedが真の場合は"Show all"、偽の場合は"Hide completed"が表示される -->
    {{ hideCompleted ? 'Show all' : 'Hide completed' }}
  </button>
</template>

<style>
.done {
  text-decoration: line-through;
}
</style>