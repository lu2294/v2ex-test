<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {
  }
}
</script>

<style>
body {
    padding: 0px;
    margin: 0px;
    /* font-family: "Helvetica Neue", "Luxi Sans", "DejaVu Sans", "Segoe UI", "Hiragino Sans GB", "Microsoft Yahei", sans-serif; */
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
