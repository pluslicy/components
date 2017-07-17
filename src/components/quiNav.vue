<template>
  <div class="qui-nav">
    <a href="javascript:void(0);" v-on:click="navClickEvent(items,index)" v-for="(item , index) in items" :class="[commonClass,item.active?'active':'']">
        <span class="nav-txt">{{item.text}}</span>
    </a>
  </div>
</template>
<script>
  export default {
    methods:{
      navClickEvent:function(items,index){
        items.forEach(function (item) {
            item.active = false;
        });
        items[index].active = true;
        this.$emit('navClickEvent',items,index)
      }
    },
    data : function () {
      return {
        commonClass:'nav-item',
        activeClass:'active',
        items: [
          {
            text: '首页',
            active : true
          }, {
            text: '列表',
            active : false
          }, {
            text: '关于',
            active : false
          }, {
            text: '招聘',
            active : false
          }
        ]
      }
    }
  }

</script>
<style scoped>
  @import './css/reset.css';
  @import './css/quiNav.css';

</style>
