<template>
  <div id="section-2" v-waypoint="{ active: true, callback: onWaypoint}">
    <div class="clock">
      <i class="far fa-clock"></i>
    </div>
    <div class="title">
      HORARIO DE ATENCIÓN
    </div>
    <div class="container">
      <div class="row">
        <div v-for="(item, key) of schedule" class="col-sm-5  day" :key="key" >
          <p>
            <label>{{item.day}}<br><label v-if="item.notes">{{item.notes}}</label></label>
          </p>
          <p>
            <label>MAÑANA</label>
            <br>
            <label>{{item.open}}</label>
          </p>
          <p>
            <label>TARDE</label>
            <br>
            <label>{{item.close}}</label>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      schedule: [
        {
          day: 'LUNES - SABADO',
          notes: ' ',
          open: '7:00 am - 12:00 pm',
          close: '2:00 pm - 7:00 pm'
        },
        {
          day: 'DOMINGO',
          notes: '(Cuando el lunes es festivo)',
          open: '7:00 am - 12:00 pm',
          close: '2:00 pm - 4:00 pm'
        }
      ]
    };
  },
  methods: {
    onWaypoint({ going, direction }) {
      console.log('SECCION 2');
      this.$emit('setDarkMenu', going === this.$waypointMap.GOING_IN);
    }
  }
};
</script>
<style scoped>
#section-2 {
  background-color: #232322;
  padding: 60px 0px;
}
.fa-clock {
  font-size: 40px;
}
.title,
.clock {
  width: 100%;
  text-align: center;
  color: #ffffff;
  font-size: 20px;
}
.title {
  padding: 20px 0px;
}
@media (min-width: 576px) {
  .row .day:first-child {
    margin-left: calc(7%);
  }
}

.day {
  color: #ffffff;
  text-align: center;
  background-color: #101010;
  margin: 15px;
  padding: 30px 15px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
}
.day p:first-child {
  min-height: 44px;
}
.day p label:last-child {
  font-weight: bold;
}
</style>
