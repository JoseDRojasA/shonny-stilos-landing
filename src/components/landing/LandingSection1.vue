<template>
  <div class="full-section">
    <div class="shadow"></div>
    <nav>
      <table>
        <tbody>
          <td>
            <img class="logo" src="./../../assets/logo_3.png">
          </td>
          <td>
            <label>M <i class="fas fa-bars"></i> NU</label>
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
export default {};
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
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.6);
}
nav {
  text-align: right;
  position: absolute;
}
nav table {
  width: 100vw;
}
nav table td {
  padding: 30px 30px;
}
nav table td:first-child {
  text-align: left;
}
nav table td:last-child {
  color: #ffffff;
  font-weight: bold;
}
nav table td:last-child label {
  cursor: pointer;
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
