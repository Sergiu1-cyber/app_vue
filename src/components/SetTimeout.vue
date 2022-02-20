<template>
  <h2>Functia: setTimeout()</h2>
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
        this.a += 3
        this.b = setTimeout(this.Start, 500)
      },
      Stop() {
        clearTimeout(this.b)
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
