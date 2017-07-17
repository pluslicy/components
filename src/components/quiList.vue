<template>
  <div class="qui-list">
    <!--
    <div>
      <span class="list-tips">{{tipsText}}</span>
      <qui-btn v-on:btnClickEvent="btnClickEvent" :msg=msg class="small"></qui-btn>
    </div>
    -->
    <div>
      <span class="list-tips">{{tipsText}}</span>
      <!--动态组件-->
      <component :is="currentView" keep-alive></component>
    </div>

  </div>
</template>

<script>
  import quiButton from '../components/quiButton.vue'
  import quiArrow from '../components/quiArrow.vue'

  export default{
    props:{
      msg: {
        default: '下载'
      },
      tipsText: {
        default: '默认的文案'
      },
      currentView:{
        default: 'qui-btn'
      }
    },
    components: {
      'qui-btn': quiButton,
      'qui-arrow':quiArrow
    },
    methods:{
      btnClickEvent:function(){
        alert('按钮点击事件')
      }
    }
  }
</script>
<style scoped>

</style>
