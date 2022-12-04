<template>
  <div id="app">
    <HeaderComp/>
    <MainComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
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
  width: 60%;
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
