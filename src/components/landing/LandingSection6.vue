<template>
  <div id="section-6" class="container-fluid" v-waypoint="{ active: true, callback: onWaypoint}">
    <div class="row">
      <div class="col-sm-6 title-container">
          <div class="row">
            <div class="col-sm-12">
              <label class="title">CONTACTO</label>
            </div>
            <div class="col-sm-12">
              <table>
                <tbody>
                  <tr>
                    <td>
                      Teléfono:
                    </td>
                    <td>
                      +57 (037) 652-40-61
                    </td>
                  </tr>
                  <tr>
                    <td>
                      Dirección:
                    </td>
                    <td>
                      Calle 50 N 21 - 82 (Bucaramanga)
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

      </div>
      <div class="col-sm-6 map-container">
        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d2287.0837117584642!2d-73.11815100751019!3d7.11335233555937!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x1d85adc9026fb1ec!2sShonny+Stilos!5e0!3m2!1ses-419!2sco!4v1517086275919" width="100%" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
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
#section-6 {
  background-color: #141414;
  padding: 60px 0px;
  border-top: 1px solid #585859;
}

.title-container label.title {
  color: #3b3b3b;
  font-weight: bolder;
  font-size: 50px;
  border-bottom: 1px solid #4d4d4d;
}
@media (min-width: 700px) {
  .title-container label.title {
    font-size: 65px;
  }
}
@media (min-width: 830px) {
  .title-container label.title {
    font-size: 80px;
  }
}
@media (min-width: 1049px) {
  .title-container label.title {
    font-size: 100px;
  }
}
.title-container table {
  color: #818181;
  margin: 0 auto;
  padding-top: 30px;
}
.map-container {
  padding: 30px;
}
</style>
