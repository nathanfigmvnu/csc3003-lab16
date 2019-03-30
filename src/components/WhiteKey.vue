<template>
  <div @mousedown="play()" @mouseup="stop()" class="whitekey">
  </div>
</template>

<script>
export default {
  name: 'WhiteKey',
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
.whitekey {
  background-color: #FDFDFD;
  border: 1px solid;
  width: 100px;
  height: 500px;
  cursor: pointer;
}
.whitekey:active {
  background-color: #CCC;
}
</style>
