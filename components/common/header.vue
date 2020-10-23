<template>
  <div>
    <div class="h-main">
      <div class="h-flex">
        <div class="h-l" @click="goBack()">返回</div>
        <div class="h-c">{{title}}</div>
        <div class="h-r">帮助</div>
      </div>
    </div>
    <div class="xm-h"></div>
  </div>
</template>

<script>
  export default {
    props: ['title'],
    methods:{
      goBack(){
        this.$router.go(-1);
      }
    }
  }
</script>

<style scoped>
  .h-main{
    position: fixed;
    width: 100%;
    top: 0;
  }
  .h-flex{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.8rem;
    box-sizing: border-box;
    background: #53abee;
    color: #ffffff;
  }
  .h-l{}
  .h-c{}
  .h-r{}
  .xm-h{
    height: 3rem;
  }
</style>
