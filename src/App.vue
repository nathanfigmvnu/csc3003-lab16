<template>
  <div id="app">
    <div class="board">
      <WhiteKey class="c4" v-bind:frequency="261" />
      <BlackKey class="c_4" v-bind:frequency="277" />
      <WhiteKey class="d4" v-bind:frequency="294" />
      <BlackKey class="d_4" v-bind:frequency="311" />
      <WhiteKey class="e4" v-bind:frequency="329" />
      <WhiteKey class="f4" v-bind:frequency="349" />
      <BlackKey class="f_4" v-bind:frequency="370" />
      <WhiteKey class="g4" v-bind:frequency="392" />
      <BlackKey class="g_4" v-bind:frequency="415" />
      <WhiteKey class="a4" v-bind:frequency="440" />
      <BlackKey class="a_4" v-bind:frequency="466" />
      <WhiteKey class="b4" v-bind:frequency="494" />
      <WhiteKey class="c5" v-bind:frequency="523" />
      <BlackKey class="c_5" v-bind:frequency="554" />
      <WhiteKey class="d5" v-bind:frequency="587" />
      <BlackKey class="d_5" v-bind:frequency="622" />
      <WhiteKey class="e5" v-bind:frequency="659" />
      <WhiteKey class="f5" v-bind:frequency="698" />
      <BlackKey class="f_5" v-bind:frequency="740" />
      <WhiteKey class="g5" v-bind:frequency="784" />
      <BlackKey class="g_5" v-bind:frequency="831" />
      <WhiteKey class="a5" v-bind:frequency="880" />
      <BlackKey class="a_5" v-bind:frequency="932" />
      <WhiteKey class="b5" v-bind:frequency="988" />
    </div>
  </div>
</template>

<script>
import WhiteKey from './components/WhiteKey.vue'
import BlackKey from './components/BlackKey.vue'
export default {
  name: 'app',
  components: {
    WhiteKey,
    BlackKey
  }
}
</script>

<style>
.board {
  display: flex;
}
</style>
