<template>
  <div @mousedown="play()" @mouseup="stop()" class="blackkey">
  </div>
</template>

<script>
export default {
  name: 'BlackKey',
  props: {
    frequency: Number
  },
  data: function() {
    return {
      oscillator: null,
      context: null,
      started: false
    }
  },
  methods: {
    play: function() {
      this.oscillator.connect(this.context.destination); 
      if (!this.started) {
        this.oscillator.start();
        this.started = true;
      }
    },
    stop: function() {
      this.oscillator.disconnect(this.context.destination);
    }
  },
  mounted() {
    this.context = new (window.AudioContext || window.webkitAudioContext)();
    this.oscillator = this.context.createOscillator(); 
    this.oscillator.type = 'sine';
    this.oscillator.frequency.value = this.frequency;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.blackkey {
  background-color: #111;
  border: 1px solid #FFF;
  width: 60px;
  height: 300px;
  z-index: 10;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  cursor: pointer;
}
.blackkey:active {
  background-color: #333;
}
</style>
