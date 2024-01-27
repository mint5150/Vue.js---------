<script setup>
  // ref関数を読み込み
  import { ref } from 'vue'

  // ref関数にtitleをセットして定数titleClassに格納
  const titleClass = ref('title')
  </script>

  <template>
    <!-- h1タグの属性にv-bind:(省略形は:)を指定 -->
    <!-- 値に定数titleClassをセット -->
    <h1 :class="titleClass">Make me red</h1>
  </template>

  <!-- styleタグの中には通常通りCSSを記述する -->
  <style>
  .title {
    color: red;
  }
  </style>