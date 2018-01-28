<template>
  <div id="section-4" class="container-fluid" v-waypoint="{ active: true, callback: onWaypoint}">
    <div class="row">
      <div class="col-sm-12 title-container">
        <p class="title">NUESTRO EQUIPO</p>
      </div>
    </div>
    <div class="row">
      <div v-for="(item, key) in hairdressers" :key="key" class="col-sm-6 col-md-4 col-lg-3 hairdresser-card" v-bind:style="{ 'background-image': 'url(' + item.img + ')'}">
        <div class="shadow">
        </div>
        <p class="name">
          <label>{{item.names}}</label>
          <br>
          <label>{{item.telephone}}</label>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hairdressers: [
        {
          names: 'SONIA',
          telephone: '316-397-1805',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo'
        },
        {
          names: 'AlIX',
          telephone: '316-830-7427',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo para alix.'
        },
        {
          names: 'OLGA',
          telephone: '318-523-0651',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo'
        },
        {
          names: 'VIVIANA',
          telephone: '317-697-8467',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo para alix.'
        },
        {
          names: 'YURLEY',
          telephone: '315-842-8052',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo'
        },
        {
          names: 'YAZMIN',
          telephone: '318-253-1695',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo para alix.'
        },
        {
          names: 'PATRICIA',
          telephone: '316-808-5122',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo'
        },
        {
          names: 'LIZZA',
          telephone: '312-501-9066',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo para alix.'
        },

        {
          names: 'YESENIA',
          telephone: 'Por definir',
          img:
            'https://www.ihdimages.com/wp-content/uploadsktz/2017/09/cute-girl-1.jpg',
          description: 'Esta es una descripción de ejemplo para alix.'
        }
      ]
    };
  },
  methods: {
    onWaypoint({ going, direction }) {
      this.$emit('setDarkMenu', going === this.$waypointMap.GOING_IN);
    }
  }
};
</script>

<style scoped>
#section-4 {
  background-color: #141414;
  padding-bottom: 55px;
}
.title-container {
  text-align: center;
}
.title {
  color: #3b3b3b;
  font-weight: bolder;
  font-size: 35px;
  margin: 25px 45px 25px 0px;
}
@media (min-width: 400px) {
  .title {
    font-size: 50px;
  }
}
.hairdresser-card {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  min-height: 400px;
  padding: 10px 30px;
  transition: all 0.5s;
}
.hairdresser-card:hover {
  -webkit-transform: scale(1.1);
  -ms-transform: scale(1.1);
  transform: scale(1.1);
  z-index: 2;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
}
.hairdresser-card .name {
  color: #ffffff;
  position: absolute;
  font-weight: bold;
  margin: 0px;
}
.hairdresser-card .name label:first-child {
  font-size: 30px;
}
.hairdresser-card .name label:last-child {
  font-size: 15px;
}
.shadow {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
}
.shadow:hover {
  background-color: rgba(0, 0, 0, 0);
}
</style>
