<template>
  <div id="app">
    <app-header/>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    AppHeader
  }
}
</script>

<style>
/* reset.css 파일을 가져온다.*/
@import "./styles/reset.css";
#app{
  width: 560px;
  margin: 0 auto;
}
</style>
