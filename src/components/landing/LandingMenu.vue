<template>
  <div id="menu" class="overlay" v-bind:class="{ active: open }">
    <a v-on:click="closeMenu()" class="closebtn">&times;</a>
    <div class="overlay-content">
      <a v-on:click="closeMenu()" href="#section-1">BIENVENIDOS</a>
      <a v-on:click="closeMenu()" href="#section-2">HORARIO DE ATENCIÓN</a>
      <a v-on:click="closeMenu()" href="#section-3">QUIENES SOMOS</a>
      <a v-on:click="closeMenu()" href="#section-4">NUESTRO EQUIPO</a>
      <a v-on:click="closeMenu()" href="#section-5">SERVICIOS</a>
      <a v-on:click="closeMenu()" href="#section-6">CONTACTO</a>
      {{open}}
    </div>
  </div>
</template>

<script>
export default {
  props: ['open'],
  methods: {
    closeMenu() {
      this.$emit('closeMenu', false);
    }
  }
};
</script>

<style scoped>
#menu {
  position: fixed;
  z-index: 101;
  width: 0%;
}
#menu.active {
  width: 100%;
}
.overlay {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: rgb(0, 0, 0);
  background-color: rgba(0, 0, 0, 0.9);
  overflow-x: hidden;
  transition: 0.5s;
}

.overlay-content {
  position: relative;
  top: 25%;
  width: 100%;
  text-align: center;
  margin-top: 30px;
}

.overlay a {
  padding: 8px;
  text-decoration: none;
  font-size: 36px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.overlay a:hover,
.overlay a:focus {
  color: #f1f1f1;
}
.closebtn {
  cursor: pointer;
}
.overlay .closebtn {
  position: absolute;
  top: 20px;
  right: 45px;
  font-size: 60px;
}

@media screen and (max-height: 450px) {
  .overlay a {
    font-size: 20px;
  }
  .overlay .closebtn {
    font-size: 40px;
    top: 15px;
    right: 35px;
  }
}
</style>
