<script setup>
//JSConfetti パッケージを 'js-confetti' から読み込み
import JSConfetti from 'js-confetti'

//JSConfetti パッケージのインスタンスを生成
const confetti = new JSConfetti()

//Confetti を表示する関数を定義
function showConfetti() {
  //SConfetti ライブラリの addConfetti メソッドを呼び出し
  confetti.addConfetti()
}
//コンポーネントがマウントされた直後に Confetti を表示
//showConfetti()
</script>

<template>
  <!-- クリック時にshowConfetti関数が呼ばれるように設定 -->
  <h1 @click="showConfetti">🎉 Congratulations!</h1>
</template>

<style>
h1 {
  text-align: center;
  cursor: pointer;
  margin-top: 1em;
  margin-bottom: 1em;
}
</style>