<template>
  <div class="display">
    <h1>Result</h1>
    <h2 class="animate__animated animate__fadeInUp">記録    {{beforeTime}}</h2>
    <button v-button @click="next">Back to Start Display</button>
    <button v-button @click="nextGame">Again</button>
  </div>
</template>

<script>
export default {
  props: ['beforeTime'],
  methods: {
    next() {
      this.$emit('toStart')
    },
    nextGame() {
      this.$emit('Again')
    }
  }
}
</script>

<style scoped>
.display {
  background-color: rgba(240, 180, 180, 0.3);
  height: 100vh;
}
.animate__animated.animate__fadeInUp {
  --animate-duration: 1.5s;
}
</style>