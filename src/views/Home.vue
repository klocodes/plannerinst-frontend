<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  mounted() {
    this.axios.get('http://backend.plannerinst.loc/api/v1/auth/user').then(response => {
      console.log(response);
    }).catch(error => {
      console.log(error.response);
    });
  }
}
</script>
