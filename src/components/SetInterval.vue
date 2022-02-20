<template>
  <h2>Functia: setInterval()</h2>
  <div id="test" :style="{marginLeft: a + 'px'}"></div>
  <br />
  <button @click="Start">Start</button>
  <button @click="Stop">Stop</button>
</template>

<script>
  export default {
    data() {
      return {
        a: 0,
        b: ''
      }
    },
    methods: {
      Start() {
        this.b = setInterval(
          () => {this.a += 3},
          500)
      },
      Stop() {
        clearInterval(this.b)
      }
    },
    mounted() {
      this.Start()
    }
  }
</script>

<style scoped>
  #test {
    width: 30px;
    height: 30px;
    background-color: #3cca07;
  }
</style>
