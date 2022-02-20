<template>
  <div class="home">
    <h1>This is an Home page</h1>
    <SetInterval />
    <Ceas1 />
    <SetTimeout />
    <Cronometru />
  </div>
</template>

<script>
// @ is an alias to /src
import SetInterval from '@/components/SetInterval.vue'
import Ceas1 from '@/components/Ceas1.vue'
import SetTimeout from '@/components/SetTimeout.vue'
import Cronometru from '@/components/Cronometru.vue'

export default {
  name: 'Home',
  components: {
    SetInterval,
    Ceas1,
    SetTimeout,
    Cronometru
  }
}
</script>
