<template>
  <div class="w-100">
    <nav class="w-50 h-100 f-bw">
      <img id="logo" src="../assets/img/logo.png" alt="logo">
      <ul>
        <NavElem
        v-for="(elements, index) in paths"
        :NavData="elements"
        :key="index"
        />
      </ul>
    </nav>
  </div>
</template>

<script>
import NavElem from "./elements/NavElem.vue"

export default {
  name: 'HeaderComp',
  components: {
    NavElem,
  },
  data(){
    return {
      paths: [
        {
          img : "img/home.png",
          title: "Home"
        },
        {
          img: "img/document.png",
          title: "Pages"
        },
        {
          img : "img/printer.png",
          title: "Blog"
        },
        {
          img : "img/cart.png",
          title: "Shop"
        },
        {
          img : "img/lab.png",
          title: "Shortcodes"
        },
        {
          img : "img/chat.png",
          title: "Support"
        },
        {
          img : "img/envelope.png",
          title: "Contact"
        }




      ]
    }
  }
}
</script>

<style scoped lang="scss">
  div{
    height: 100px;
  }
  #logo{
    height: 80px;
  }
  // sprites
  #contacts{
    background: url("../assets/img/envelope.png") 0 0;
  }



  .sprites{
    height: 32px;
    width: 32px;
  }

  ul{
    display: flex;
    list-style: none;
    height: 100%;
  }

  li{
    padding: 0 15px;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    div{
      border: none;
    }
  }


  
</style>
