<template>
  <div id="test">Ora: {{time}}</div>
</template>

<script>
  export default {
    data() {
      return {
        time: ''
      }
    },
    methods: {
      SetTime() {
        setInterval(
          () => {
            this.time = new Date().toLocaleTimeString()
          }, 1000 )
      }
    },
    mounted() {
      this.SetTime()
    }
  }
</script>

<style scoped>

</style>
