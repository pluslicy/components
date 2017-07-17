<template>
  <div id="pageQuiButton">
    <!--使用-->
    <qui-btn msg="取消" class="small">
      <img slot="icon" class="ico" src="../assets/btn-icon1.png" />
    </qui-btn>
    <qui-btn msg="确定" class="small"></qui-btn>
    <qui-btn v-on:btnClickEvent="doSth" msg="重置" class="small"></qui-btn>
  </div>
</template>

<script>
  import quiBtn from '../components/quiButton.vue' /*引用*/
  export default {
    name: 'pageQuiButton',
    components: {
      'qui-btn': quiBtn /*注册自定义标签*/
    },
    methods:{
        doSth: function(){
            alert("this is pageQuiButton");
        }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import './css/reset.css';

</style>
