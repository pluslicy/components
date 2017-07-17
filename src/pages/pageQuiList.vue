<template>
  <div class="">
    <qui-list></qui-list>
    <qui-list tipsText="自定义文案，默认右边是按钮" msg="弹层"></qui-list>
    <qui-list ref="child1" tipsText="最右边是箭头" currentView="qui-arrow"></qui-list>

  </div>
</template>

<script>
  import quiList from '../components/quiList.vue' /*引用*/
  export default {
    name: 'hello',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    components:{
        'qui-list':quiList
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import './css/reset.css';

</style>
