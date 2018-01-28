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
}
html {
  scroll-behavior: smooth;
}
.row {
  margin: 0;
}
.full-section {
  width: 100%;
  height: 100vh;
}
* {
  font-family: 'Open Sans', sans-serif;
}
</style>
