<template lang="pug">
  #app
    #nav
    .pageContainer
      img.pic.pic1(src="./assets/ps.png" width="70" alt="一張圖片")
      img.pic.pic2(src="./assets/arduino.png" width="70" alt="一張圖片")
      img.pic.pic3(src="./assets/dev.png" width="70" alt="一張圖片")
      img.pic.pic4(src="./assets/vsc.png" width="70" alt="一張圖片")
      .menuList
        router-link.menu(v-for="item in menu" :to="{path:'/'+item.id}" :key="item.id")
          .menuItem {{item.title}}
      .pageName
        .eng NTHU IPTA
        .chi 藝術學院學士班
      router-view
</template>
<script>
export default {
  data(){
    return {
      menu: [
        {title: 'Home', id:''},
        {title: '招生', id:'student'},
        {title: '課程', id:'course'},
        {title: '師資', id:'teacher'},
        {title: '範例&聯絡', id:'example'}
      ]
    }
  }
}
</script>
<style lang="sass">
#app 
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  background-color: #888888

#nav 
  padding: 30px


#nav a 
  font-weight: bold
  color: #2c3e50


#nav a.router-link-exact-active 
  color: #42b983

.pageContainer
  background-color: #ccc
  width: 90%
  margin: auto
  padding-bottom: 50px
  position: relative
.pic
  position: absolute
.pic1
  left: 5px
  top: 700px
.pic2
  left: 10px
  top: 1200px
.pic3
  right: 8px
  top: 400px
.pic4
  right: 5px
  top: 1000px
.menuContainer
  display: flex
  flex-direction: row
  justify-content: flex-end
.menuItem
  padding: 15px 20px
  font-size: 24px
  position: relative
.menuItem:hover
  background-color: #ddd
  .menuListContainer
    display: block
.menuListContainer
  display: none
  min-width: 220px
  position: absolute
  background-color: #ddd
  left: 0px
  top: 60px
.menuList
  padding: 10px 15px
  border: 7px solid #eee
.pageName
  width: 80%
  margin: auto
  margin-top: 50px
  border: 5px solid #FFF
  padding: 50px 30px
  margin-bottom: 200px
.eng
  font-size: 120px
  margin-bottom: 40px
.chi
  font-size: 40px
</style>
