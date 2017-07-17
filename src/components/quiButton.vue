<template>
  <button class="qui-btn" v-on:click="btnClickEvent">
    <slot name="icon"></slot><!--这里是插槽！重点在这里-->
    <span>{{msg}}</span>
  </button>
</template>

<script>
  export default {
    props: {
      msg: {
        default: '下载'
      }
    },
    methods: {    //绑定事件的关键代码
      btnClickEvent: function(){
        alert("this is quiButton",this.msg);
        //发射
        this.$emit('btnClickEvent');
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import './css/quiButton.css';

</style>
