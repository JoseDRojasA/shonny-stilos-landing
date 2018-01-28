<template>
  <div id="section-3" class="container-fluid" v-waypoint="{ active: true, callback: onWaypoint}">
    <div class="row">
      <div class="col-sm-6 picture">
      </div>
      <div class="col-sm-6 content">
        <p class="title">
          QUIENES SOMOS
        </p>
        <p>
          Shonny Stilos fue fundada en el año 1988 por Sonia Rocio Aguilar Mosquera junto a su hermana y socia, Alix Meiby Aguilar Mosquera.
        </p>
        <p>
          Nuestra misión es ser una de las salas de belleza lideres en Bucaramanga donde destacamos por la calidad de los diferentes servicios que ofrecemos.
        </p>
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
.picture {
  background-image: url('./../../assets/section_3.jpg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  min-height: 200px;
}
.content {
  background-color: #f6f6f6;
  padding: 40px;
}
.content p {
  text-align: justify;
}
.title {
  color: #2b2b2b;
  font-weight: bold;
  font-size: 20px;
  margin: 60px 0px;
}
</style>
