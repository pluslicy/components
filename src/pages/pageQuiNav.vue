<template>
  <div class="">
    <qui-nav v-on:navClickEvent="doSth"></qui-nav>
  </div>
</template>

<script>
  import quiNav from '../components/quiNav.vue' /*引用*/
  export default {
    name: 'pageQuiNav',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    components: {
      'qui-nav': quiNav /*注册自定义标签*/
    },
    methods: {
      doSth:function(a,b){
          alert(1);
          console.log(a,b);
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import './css/reset.css';

</style>
