<template>
  <div class="qui-arrow" v-on:click="btnClickEvent">
    <span>{{msg}}</span>
    <span>&gt;&gt;</span>
  </div>
</template>

<script>
  export default {
    props: {
      msg: {
        default: '更多'
      }
    },
    methods: {    //绑定事件的关键代码
      btnClickEvent: function(){
        //发射
        this.$emit('btnClickEvent');
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
