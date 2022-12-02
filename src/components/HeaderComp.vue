<template>
  <div class="w-100">
    <nav class="w-70 h-100 f-bw">
      <img id="logo" src="../assets/img/logo.png" alt="logo">
      <ul>
        <li>
          Home
        </li>
        <li>
          Pages
        </li>
        <li>
          Blog
        </li>
        <li>
          Shop
        </li>
        <li>
        Shortcodes
        </li>
        <li>
          Support
        </li>
        <li>
          Contact
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'HeaderComp',
 
}
</script>

<style scoped lang="scss">
  div{
    height: 100px;
  }

  #logo{
    height: 80px;
  }

  ul{
    display: flex;
    list-style: none;
  }

  li{
    margin: 0 10px;
  }
</style>
