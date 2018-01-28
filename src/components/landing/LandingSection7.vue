<template>
  <div id="section-7" class="container-fluid" v-waypoint="{ active: true, callback: onWaypoint}">
    <div class="row">
      <div class="col-sm-12">
        <label>SIGUENOS EN NUESTRAS REDES SOCIALES</label>
      </div>
      <div class="col-sm-12 social-container">
        <a href="https://www.facebook.com/shonny.stilos?ref=br_rs" target="_blank">
          <i class="fab fa-facebook-square"></i>
        </a>
        <a href="https://www.instagram.com/shonnystilos/" target="_blank">
          <i class="fab fa-instagram"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    onWaypoint({ going, direction }) {
      this.$emit('setDarkMenu', going === this.$waypointMap.GOING_IN);
    }
  }
};
</script>

<style scoped>
#section-7 {
  background-color: #000000;
}
.row {
  text-align: center;
  padding: 30px 0px;
}
.row div:first-child {
  padding-bottom: 20px;
}
label {
  color: #737373;
  letter-spacing: 5px;
}
.social-container svg {
  color: #737373;
  font-size: 30px;
  cursor: pointer;
  margin: 0 15px;
}
</style>
