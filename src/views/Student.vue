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
      title: '招生Q&A',
      news: [
        {title: '1.請問藝術學院學士班與藝設系有何不同？', content: 'A：(1)藝術學院學士班主要強調當代藝術中的新形式創作-科技藝術(Technology Art)，亦即運用科技媒介（如感測器晶片、網路、虛擬實境 …）從事創作。(2)藝設系主要有油畫、版畫、雕塑等專業課程以及各類工藝專業課程（木藝、玻璃藝術設計、陶瓷藝術設計…等）。'},
        {title: '2.請問藝術學院學士班與清華學院的美資班有何不同？', content: 'A：(1)藝術學院學士班說明如上，藝術學院有專屬教師，也特別開出的「科技藝術」跨域課程。(2)清華學院的美資班課程設計為多元，師資與課程來自各學院。'},
        {title: '3.請問學士班是否大二後會做分流？', content:'A：(1)本院學士班主要把「科技藝術」跨域當成專業領域來培育人才，因此不做分流。(2)學生未來若志趣不合，可透過轉系方式轉至感興趣之學系就讀。'}
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
.newsText
  width: 200%
  text-align: left
  font-size: 18px
  line-height: 28px
.newsTitle
  color: #2A74B8
</style>
