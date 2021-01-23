<template lang="pug">
  .homeContainer
    .homeTitle {{title}}
    .news(v-for="item in news")
      .newsImg(:style="{'background-image': 'url(' + item.img + ')'}")
      .newsText
        .newsTitle {{item.title}}
        .newsContent {{item.content}}
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data(){
    return {
      title: '院學士班最新消息',
      news: [
        {title: '《那顆Ｇ1咻！》國立清華大學藝術學院學士班第一屆系展', img: 'https://scontent.ftpe7-3.fna.fbcdn.net/v/t1.0-9/139503332_2131733390289905_6942051494522370880_o.jpg?_nc_cat=102&ccb=2&_nc_sid=730e14&_nc_ohc=O7EOLZDiPdAAX_WAFqh&_nc_ht=scontent.ftpe7-3.fna&oh=4ebfd21d3a208c9a8e2faf56daa6e2f6&oe=602F6F0E', content: '「當藝術碰撞科技，會迸出什麼樣的火花呢?」「科技藝術跨領域創作」一直以來為學士班重要的創作方向，同學們將於系展中利用所學，展現創作熱誠與思維，分享作品中科技與藝術接軌的威力！'},
        {title: '《科技物件與人類幻象》講座與工作坊', img: 'https://scontent.ftpe7-1.fna.fbcdn.net/v/t1.0-9/140295130_2131733323623245_5975443460875073963_o.jpg?_nc_cat=110&ccb=2&_nc_sid=730e14&_nc_ohc=IGs774DdIKMAX_uKca8&_nc_ht=scontent.ftpe7-1.fna&oh=1fa8903cb91accae94e915c633cd875c&oe=602ED7F1', content: '【演講題目】:爬行者:1 – Crawler:1網際網路蓬勃以及硬軟體技術發展，2013年至2020年資料量將成長10倍，總量將從4.4ZB增加至44ZB。「你的資料就是我的資料。」右鍵另存新檔的時代已過去，網路爬蟲將幫助分散式使用者取得網路上大量的資料，讓資料得以成為素材去進行創造。現代人的一舉一動...'}
      ]
    }
  }
}
</script>
<style lang="sass">
.homeContainer
  width: 80%
  padding: 30px
  margin: auto
  background-color: #fff
.homeTitle
  margin-top: 50px
  font-size: 40px
  font-weight: bold
.news
  width: 80%
  margin: auto
  padding: 50px 70px
  background-color: #d3e5eb
  margin-top: 70px
  margin-bottom: 50px
  display: flex
  flex-direction: row
  justify-content: space-between
  align-items: center
.newsImg
  width: 30%
  height: 200px
  background-size: cover
.newsText
  width: 65%
  text-align: left
  font-size: 18px
  line-height: 28px
.newsTitle
  color: #2A74B8
</style>
