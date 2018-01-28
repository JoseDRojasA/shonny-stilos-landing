<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
};
</script>

<style>
@import url('./assets/bootstrap-grid.min.css');
body {
  margin: 0;
  overflow-x: hidden;
}
html {
  scroll-behavior: smooth;
}
.full-section {
  width: 100vw;
  height: 100vh;
}
* {
  font-family: 'Open Sans', sans-serif;
}
</style>
