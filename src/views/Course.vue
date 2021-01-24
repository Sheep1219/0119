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
      title: '學士班課程',
      news: [
        {content:'本學院107學年度成立藝術學院〝科技藝術〞跨域學士班，學院率領一群科技藝術「已經跨域」教師與業界顧問擔任專兼任老師，開出一些「已經跨域」的課程，希望培養一群臺灣科技藝術的尖兵。'},
        {content:'課程設計兼顧跨領域（transdisciplinary）與多領域（multi-disciplinary）。學位：科技藝術學士學位 （Bachelor of Science and Art）第二專長學士學位（若學生有另選第二專長課程）'}
      ]
    }
  }
}
</script>
<style lang="sass">

</style>
