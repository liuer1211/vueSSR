<template>
  <div class="container">
    <headers :title="title"/>
    <!--banner-->
    <div class="a-main">
      <div class="a-switch">
        <img class="a-switch-img" alt="banner" src="../../assets/imges/about/ad1.jpg" title="banner"/>
      </div>
    </div>
    <!--list-->
    <div class="a-list-main">
      <div class="a-list-model" v-for="(item,index) in list" :key="index">
        <div class="a-list-model-l">
          <img class="a-list-t-img" :src="item.imgUrl"/>
        </div>
        <div class="a-list-model-r">
          <h1>{{item.title}}</h1>
          <div>{{item.cen}}</div>
        </div>
      </div>
    </div>
    <!--other-->
    <div class="a-other-main">
      <div class="a-other-up">
        <div class="a-other-up-l">其他</div>
        <div class="a-other-up-r">更多>></div>
      </div>
      <div class="a-other-bot">
        <div class="a-other-bot-model" v-for="(item,index) in list" :key="index">
          <img class="a-other-bot-img" :src="item.imgUrl"/>
          <span class="a-other-bot-name">{{item.title}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import headers from '~/components/common/header.vue'
  export default {
    components:{
      headers
    },
    data(){
      return {
        title: '关于',
        list:[
          {
            imgUrl: '_nuxt/assets/imges/about/ad1.jpg',
            title: '快乐学习',
            cen: '好好学习，天天向上'
          },
          {
            imgUrl: '_nuxt/assets/imges/about/ad1.jpg',
            title: '快乐学习',
            cen: '好好学习，天天向上'
          },
          {
            imgUrl: '_nuxt/assets/imges/about/ad1.jpg',
            title: '快乐学习',
            cen: '好好学习，天天向上'
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .container{}
  .a-main{}
  .a-switch{
    margin: 0.8rem;
    box-sizing: border-box;
    background: #D9F3E7;
    border-radius: 0.3rem;
  }
  .a-switch-img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 0.3rem;
    display: block;
  }
  .a-list-main{}
  .a-list-model{
    display: flex;
    padding: 0.8rem;
    box-sizing: border-box;
    border-top: 0.1rem solid #f1f1f1;
  }
  .a-list-model:last-child{
    border-bottom: 0.5rem solid #f1f1f1;
  }
  .a-list-model-l{
    flex: 1;
  }
  .a-list-t-img{
    width: 6rem;
    min-width: 6rem;
    height: 5rem;
    object-fit: cover;
    border-radius: 0.3rem;
  }
  .a-list-model-r{
    flex: 3;
    padding: 0.2rem 0.8rem;
    box-sizing: border-box;
  }
  h1{
    font-size: 1.2rem;
    margin-bottom: 0.2rem;
  }
  .a-other-main{
    padding: 0.8rem;
  }
  .a-other-up{
    display: flex;
    justify-content: space-between;
    margin: 0 0 0.8rem;
  }
  .a-other-up-l{

  }
  .a-other-up-r{
    font-size: 0.8rem;
    color: #828282;
  }
  .a-other-bot{
    display: flex;
  }
  .a-other-bot-model{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0 0.3rem;
  }
  .a-other-bot-img{
    width: 5rem;
    height: 5rem;
    object-fit: cover;
    border-radius: 0.3rem;
  }
  .a-other-bot-name{
    margin: 0.2rem 0 0;
    font-size: 0.9rem;
  }
</style>
