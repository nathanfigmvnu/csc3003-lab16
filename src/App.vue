<template>
  <div id="app">
    <div class="board">
      <WhiteKey class="c4" v-bind:frequency="261" />
      <WhiteKey class="d4" v-bind:frequency="294" />
      <WhiteKey class="e4" v-bind:frequency="329" />
      <WhiteKey class="f4" v-bind:frequency="349" />
      <WhiteKey class="g4" v-bind:frequency="392" />
      <WhiteKey class="a4" v-bind:frequency="440" />
      <WhiteKey class="b4" v-bind:frequency="494" />
      <WhiteKey class="c5" v-bind:frequency="523" />
      <WhiteKey class="d5" v-bind:frequency="587" />
      <WhiteKey class="e5" v-bind:frequency="659" />
      <WhiteKey class="f5" v-bind:frequency="698" />
      <WhiteKey class="g5" v-bind:frequency="784" />
      <WhiteKey class="a5" v-bind:frequency="880" />
      <WhiteKey class="b5" v-bind:frequency="988" />
    </div>
  </div>
</template>

<script>
import WhiteKey from './components/WhiteKey.vue'
export default {
  name: 'app',
  components: {
    WhiteKey
  }
}
</script>

<style>
.board {
  display: flex;
}
</style>
