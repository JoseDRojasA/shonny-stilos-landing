<template>
  <div id="section-1" class="full-section" v-waypoint="{ active: true, callback: onWaypoint}">
    <landing-menu :open="open" @closeMenu="open = false"></landing-menu>
    <div class="shadow"></div>
    <nav>
      <table>
        <tbody>
          <td>
            <img v-if="showIcon" class="logo" src="./../../assets/logo_3.png">
          </td>
          <td v-bind:class="{'darkMenu': darkMenu}">
            <label v-on:click="open = true" >M <i class="fas fa-bars"></i> NU</label>
          </td>
        </tbody>
      </table>
    </nav>
    <div class="welcome">
      <p>
        BIENVENIDOS A
      </p>
      <p class="shonny-label">
        SHONNY STILOS
      </p>
      <p>
        <i class="fas fa-cut"></i>
      </p>
    </div>
  </div>
</template>

<script>
import LandingMenu from './LandingMenu';
export default {
  components: {
    LandingMenu
  },
  props: ['darkMenu', 'showIcon'],
  data() {
    return {
      open: false
    };
  },
  methods: {
    onWaypoint({ going, direction }) {
      this.$emit('setDarkMenu', going === this.$waypointMap.GOING_IN);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.full-section {
  background-image: url('./../../assets/section_1.jpeg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.shadow {
  position: absolute;
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.6);
}
nav {
  text-align: right;
  position: fixed;
  z-index: 100;
  width: calc(100% - 15px);
}
nav table {
  width: 100%;
}

nav table td:first-child {
  text-align: left;
  padding: 30px 0px 30px 55px;
}
nav table td:last-child {
  color: #ffffff;
  padding: 30px 0px 30px 0px;
  font-weight: bold;
  font-size: 20px;
}
.darkMenu {
  color: #3b3b3b !important;
}
nav table td:last-child label {
  cursor: pointer;
}
@media (min-width: 760px) {
  nav table td:last-child {
    padding: 30px 55px 30px 0px;
  }
}
.logo {
  max-width: 100px;
}
.welcome {
  text-align: center;
  margin: auto;
  color: #ffffff;
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  transform: translate(-50%, -50%);
}
.welcome p:first-child {
  letter-spacing: 2px;
  font-size: 24px;
}
.welcome p.shonny-label {
  font-size: 30px;
  font-weight: bolder;
  letter-spacing: 30px;
}
.welcome p:last-child {
  font-size: 30px;
}
.welcome p:last-child svg {
  transform: rotate(90deg);
}
</style>
