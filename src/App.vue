<template>
  <div id="app">
    <Navbar/>
    <router-view/>
    <GFooter/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import GFooter from "./components/GFooter";
export default {
  components : {
    Navbar , GFooter
  }
}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

html,
body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
</style>
