<template>
  <div id="app">
    <NavComponente></NavComponente>
    <router-view/>
  </div>
</template>

<script>
import NavComponente from "@/components/NavComponente.vue";
export default {
  components: {
    NavComponente
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 45px;
}
</style>
