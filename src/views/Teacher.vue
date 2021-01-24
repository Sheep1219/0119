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
        {title: '許素朱（小牛）(Su-Chu Hsu) 博士/教授 兼 院長', content:'清華大學通識教育中心/藝設系/資應所合聘教授。學歷：國立清華大學資訊科學博士專長：互動科技藝術、物聯網創意應用、數位文創產業、未來博物館、創客藝術與教育。經歷：國立台北藝術大學新媒體藝術系教授、電影與新媒體學院院長、文化部文化科技政策諮詢委員'},
        {title: '陳珠櫻 (Chu-Yin Chen)  博士/教授 兼 班主任', content:'學歷：法國巴黎第八大學藝術博士。專長：數位藝術創作、創作心理學、人工生命、認知科學、腦科學、心理現象學。經歷：法國巴黎第八大學藝術與科技影像所所長'},
        {title: '邱誌勇 (Chih-Yung Chiu)  博士/教授', content:'學歷：美國俄亥俄大學跨科際藝術系博士。專長：新媒體藝術美學、藝術評論、電影電視美學與科技文化研究曾獲第一屆與第二屆數位藝術評論獎。經歷：北京師範大學-香港浸會大學聯合國際學院文化與創意學部院長、國立台灣師範大學美術系專任教授、臺灣科技藝術學會理事長、台北數位藝術節策展人'},
        {title: '朱宏國 (Hung-Kuo Chu)  博士/副教授 (資訊工程系合聘)', content:'學歷：國立成功大學資訊科學博士。專長：人機互動(Human-Computer Interaction)、AR/VR/MR、Smart Manipulation、Visual Perception、Shape Analysis。經歷：清華大學資工系副教授、第二十六屆電腦圖學研討會(CGW 2018) Best Paper Award'},
        {title: '游創文 (Chuang-Wen You)  博士/助理教授', content:'學歷：國立臺灣大學資訊工程所博士。專長：人機互動（Human-Computer Interaction）、普及計算（Ubiquitous Computing）、無線感測網路（Sensor Networking Systems）。經歷：國立臺灣大學資訊管理學系兼任助理教授、國立臺灣大學智慧聯網創新研究中心專案計畫助理研究員、中央研究院資訊科技創新研究中心博士後研究學者、Dartmouth College訪問學者、宏達國際電子股份有限公司資深工程師'}
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
