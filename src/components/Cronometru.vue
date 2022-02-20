<template>
  <h2>{{ counter }}</h2>
  <input type="number" v-model="counter" />
  <br />
  <button @click="setCounter">Click</button>
</template>

<script>
  export default {
    data() {
      return {
        counter: '',
        b: ''
      }
    },
    methods: {
      setCounter() {
        if (this.counter==1) {
          clearTimeout(this.b)
          this.counter = "STOP"
        } else {
          this.counter -= 1
          this.b = setTimeout(this.setCounter, 1000);
        }
      }
    },
    mounted() {
      
    }
  }
</script>

<style scoped>

</style>
