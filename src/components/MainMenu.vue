<script setup>
import TipsItem from './TipsItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import Tips1 from '../views/tips1.vue'
import Tips2 from '../views/tips2.vue'
import Tips3 from '../views/tips3.vue'
import Tips4 from '../views/tips4.vue'
import Tips5 from '../views/tips5.vue'
import Tips6 from '../views/tips6.vue'
import Tips7 from '../views/tips7.vue'
import Tips8 from '../views/tips8.vue'
import Tips9 from '../views/tips9.vue'
import Tips10 from '../views/tips10.vue'
import Tips11 from '../views/tips11.vue'
import Tips12 from '../views/tips12.vue'
import Tips13 from '../views/tips13.vue'
import Tips14 from '../views/tips14.vue'
import Tips15 from '../views/tips15.vue'
</script>

<template>
<div class="all-tips">
  <TipsItem>
    <template #heading><DocumentationIcon /> 目次</template>
  </TipsItem>

  <hr>
  <TipsItem>
    <template #heading><DocumentationIcon /> Tips1:はじめに</template>
    <!-- <Tips1 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-1" target="_blank" rel="noopener">こちら</a><br>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips2:宣言的レンダリング</template>
    <!-- <Tips2 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-2" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips3:属性バインディング</template>
    <!-- <Tips3 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-3" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips4:イベントリスナー</template>
    <!-- <Tips4 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-4" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips5:フォームバインディング</template>
    <!-- <Tips5 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-5" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips6:条件付きレンダリング</template>
    <!-- <Tips6 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-6" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips7:リストレンダリング</template>
    <!-- <Tips7 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-7" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips8:算出プロパティー</template>
    <!-- <Tips8 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-8" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips9:ライフサイクルとテンプレート参照</template>
    <!-- <Tips9 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-9" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips10:ウォッチャー</template>
    <!-- <Tips10 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-10" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips11:コンポーネント</template>
    <!-- <Tips11 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-11" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips12:props</template>
    <!-- <Tips12 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-12" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips13:イベントの発行</template>
    <!-- <Tips13 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-13" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips14:スロット</template>
    <!-- <Tips14 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-14" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <TipsItem>
    <template #heading><DocumentationIcon /> Tips15:やったね！</template>
    <!-- <Tips15 /> -->
    公式リンクは<a href="https://ja.vuejs.org/tutorial/#step-15" target="_blank" rel="noopener">こちら</a>
  </TipsItem>

  <hr>

  <button @click="showComponentA">Tips1</button>
  <button @click="showComponentB">Tips2</button>
  <button @click="showComponentC">Tips3</button>
  <button @click="showComponentD">Tips4</button>
  <button @click="showComponentE">Tips5</button><br>
  <button @click="showComponentF">Tips6</button>
  <button @click="showComponentG">Tips7</button>
  <button @click="showComponentH">Tips8</button>
  <button @click="showComponentI">Tips9</button>
  <button @click="showComponentJ">Tips10</button><br>
  <button @click="showComponentK">Tips11</button>
  <button @click="showComponentL">Tips12</button>
  <button @click="showComponentM">Tips13</button>
  <button @click="showComponentN">Tips14</button>
  <button @click="showComponentO">Tips15</button>

  <hr>

  <div v-if="currentComponent === 'A'">
  <ComponentA />
  </div>
  <div v-if="currentComponent === 'B'">
  <ComponentB />
  </div>
  <div v-if="currentComponent === 'C'">
  <ComponentC />
  </div>
  <div v-if="currentComponent === 'D'">
  <ComponentD />
  </div>
  <div v-if="currentComponent === 'E'">
  <ComponentE />
  </div>
  <div v-if="currentComponent === 'F'">
  <ComponentF />
  </div>
  <div v-if="currentComponent === 'G'">
  <ComponentG />
  </div>
  <div v-if="currentComponent === 'H'">
  <ComponentH />
  </div>
  <div v-if="currentComponent === 'I'">
  <ComponentI />
  </div>
  <div v-if="currentComponent === 'J'">
  <ComponentJ />
  </div>
  <div v-if="currentComponent === 'K'">
  <ComponentK />
  </div>
  <div v-if="currentComponent === 'L'">
  <ComponentL />
  </div>
  <div v-if="currentComponent === 'M'">
  <ComponentM />
  </div>
  <div v-if="currentComponent === 'N'">
  <ComponentN />
  </div>
  <div v-if="currentComponent === 'O'">
  <ComponentO />
  </div>
  <hr>
  <br>
</div>
</template>

<style>

.all-tips {
  text-align: center;
  margin-top: 40px;
}

button {
  width: 120px;
}

</style>

<script>
import ComponentA from './ComponentA.vue';
import ComponentB from './ComponentB.vue';
import ComponentC from './ComponentC.vue';
import ComponentD from './ComponentD.vue';
import ComponentE from './ComponentE.vue';
import ComponentF from './ComponentF.vue';
import ComponentG from './ComponentG.vue';
import ComponentH from './ComponentH.vue';
import ComponentI from './ComponentI.vue';
import ComponentJ from './ComponentJ.vue';
import ComponentK from './ComponentK.vue';
import ComponentL from './ComponentL.vue';
import ComponentM from './ComponentM.vue';
import ComponentN from './ComponentN.vue';
import ComponentO from './ComponentO.vue';

export default {
  data() {
    return {
      currentComponent: ''
    };
  },
  methods: {
    showComponentA() {
      this.currentComponent = 'A';
    },
    showComponentB() {
      this.currentComponent = 'B';
    },
    showComponentC() {
      this.currentComponent = 'C';
    },
    showComponentD() {
      this.currentComponent = 'D';
    },
    showComponentE() {
      this.currentComponent = 'E';
    },
    showComponentF() {
      this.currentComponent = 'F';
    },
    showComponentG() {
      this.currentComponent = 'G';
    },
    showComponentH() {
      this.currentComponent = 'H';
    },
    showComponentI() {
      this.currentComponent = 'I';
    },
    showComponentJ() {
      this.currentComponent = 'J';
    },
    showComponentK() {
      this.currentComponent = 'K';
    },
    showComponentL() {
      this.currentComponent = 'L';
    },
    showComponentM() {
      this.currentComponent = 'M';
    },
    showComponentN() {
      this.currentComponent = 'N';
    },
    showComponentO() {
      this.currentComponent = 'O';
    }
  },
  components: {
    ComponentA,
    ComponentB,
    ComponentC,
    ComponentD,
    ComponentE,
    ComponentF,
    ComponentG,
    ComponentH,
    ComponentI,
    ComponentJ,
    ComponentK,
    ComponentL,
    ComponentM,
    ComponentN,
    ComponentO
  }
};
</script>