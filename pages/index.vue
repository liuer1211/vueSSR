<template>
  <div class="container">
    <div class="model" v-for="(item,index) in list" :key="index" @click="toPage(item)">{{item.name}}</div>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        list:[
          {
            link: 'about',
            name: '关于'
          },
          {
            link: 'news',
            name: '新闻'
          }
        ]
      }
    },
    methods:{
      toPage(item){
        this.$router.push({path: `/${item.link}`})
      }
    }
  }
</script>

<style scoped>
  .container{
    display: flex;
    flex-wrap: wrap;
    padding: 1rem;
    box-sizing: border-box;
  }
  .model{
    width: 20%;
    text-align: center;
    box-sizing: border-box;
    padding: 0.5rem;
    border-radius: 0.3rem;
    margin: 0 0.2rem;
    color: #ffffff;
    background: #0ba3f3;
  }
</style>
