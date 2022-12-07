<template>
  <div id="app">
    <HeaderComp/>
    <MainComp
    :news="news1"/>
    <FooterComp
    :news="news1"/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'
import FooterComp from './components/FooterComp.vue';

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
    FooterComp,
  },
  data(){
    return {
      news1:[
              {
                  date: "October 03, 2014",
                  img: "img/blog_09.jpg",
                  number: "42",
                  title: "Drawing and Painting Lessons",
                  author:"Anna Brown",
                  genre: "Events, Fun",
                  article: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer non dapibus augue. Praesent quam nisi, elementum at porttitor vel, lacinia sit amet enim. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Aenean a facilisis justo. Etiam rutrum egestas leo nec rutrum. Fusce massa metus, vestibulum vel metus et, rutrum varius sem. Proin sit amet leo vel lacus vestibulum aliquet nec et neque. Phasellus egestas dui tellus. Curabitur semper imperdiet nibh et ornare. Curabitur nec magna dolor. Aenean faucibus ligula arcu, id placerat metus tincidunt id. Integer sodales auctor semper. Nunc id ligula sit amet odio lacinia rutrum. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Integer dolor tortor, lobortis vitae purus id, ornare ullamcorper felis."
              },
              {
                  date: "October 03, 2014",
                  img: "img/blog_10.jpg",
                  number: "19",
                  title: "Fall Parents Meeting Day",
                  author:"Anna Brown",
                  genre: "Dance, Education",
                  article: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer non dapibus augue. Praesent quam nisi, elementum at porttitor vel, lacinia sit amet enim. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Aenean a facilisis justo. Etiam rutrum egestas leo nec rutrum. Fusce massa metus, vestibulum vel metus et, rutrum varius sem. Proin sit amet leo vel lacus vestibulum aliquet nec et neque. Phasellus egestas dui tellus. Curabitur semper imperdiet nibh et ornare. Curabitur nec magna dolor. Aenean faucibus ligula arcu, id placerat metus tincidunt id. Integer sodales auctor semper. Nunc id ligula sit amet odio lacinia rutrum. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Integer dolor tortor, lobortis vitae purus id, ornare ullamcorper felis."
              },
              {
                  date: "October 03, 2014",
                  img: "img/blog_08.jpg",
                  number: "22",
                  title: "Fall Parents Meeting Day",
                  author:"Anna Brown",
                  genre: "Games, General",
                  article: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer non dapibus augue. Praesent quam nisi, elementum at porttitor vel, lacinia sit amet enim. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Aenean a facilisis justo. Etiam rutrum egestas leo nec rutrum. Fusce massa metus, vestibulum vel metus et, rutrum varius sem. Proin sit amet leo vel lacus vestibulum aliquet nec et neque. Phasellus egestas dui tellus. Curabitur semper imperdiet nibh et ornare. Curabitur nec magna dolor. Aenean faucibus ligula arcu, id placerat metus tincidunt id. Integer sodales auctor semper. Nunc id ligula sit amet odio lacinia rutrum. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Integer dolor tortor, lobortis vitae purus id, ornare ullamcorper felis."
              }

          ],

    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.w-100{
  width: 100%;
}

.w-50{
  width: 65%;
  margin: auto;
}

.h-100{
  height: 100%;
}

.p-10{
  padding: 10px;
}
// flex
.f-bw{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.sprites{
    height: 32px;
    width: 32px;
  }

</style>
