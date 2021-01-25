<template>
  <div class="home">
    <img alt="BeeData Logo" src="../assets/logo.png"  width="75" height="75">
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/> -->


    <beedata />
  </div>
</template>

<script>
// @ is an alias to /src

import beedata from '@/components/beedata.vue'

export default {
  name: 'Home',
  components: {
    beedata
  }
}
</script>
