<template>
  <div id="app">
    <HeaderComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp
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

.w-70{
  width: 70%;
  margin: auto;
}

.h-100{
  height: 100%;
}

// flex
.f-bw{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
