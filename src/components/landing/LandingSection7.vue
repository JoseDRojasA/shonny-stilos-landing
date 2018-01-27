<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-sm-12">
        <label>SIGUENOS EN NUESTRAS REDES SOCIALES</label>
      </div>
      <div class="col-sm-12 social-container">
        <a href="https://www.facebook.com/shonny.stilos?ref=br_rs">
          <i class="fab fa-facebook-square"></i>
        </a>
        <a href="https://www.instagram.com/shonnystilos/">
          <i class="fab fa-instagram"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container-fluid {
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
