<template>
  <div class="container-fluid">
    <div class="row title-container">
      <div class="col-sm-12">
        <i class="fas fa-ticket-alt"></i>
      </div>
      <div class="col-sm-12 title">
        SERVICIOS
      </div>
    </div>
    <div class="row">
      <div class="col-sm-12 ">
        <div class="price-container">
          <table>
            <tr v-for="(item,key) of services" :key="key">
              <td>
                {{item.name}} {{dots}}
              </td>
              <td class="value">
                {{item.price | currency('', 0, { thousandsSeparator: '.' })}}
              </td>
              <td>
                {{item.min ? '*': ''}}
              </td>
            </tr>
          </table>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-12 note">
        <p>
          <label>Nota: </label>
          <label>Los servicios que poseen el simbolo '*' al lado de su valor indican que este puede variar.</label>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          name: 'Corte',
          price: 12000,
          min: true
        },
        {
          name: 'Peinado',
          price: 12000,
          min: true
        },
        {
          name: 'Planchado',
          price: 12000
        },
        {
          name: 'Cepillado',
          price: 12000
        },
        {
          name: 'Aliser',
          price: 12000,
          min: true
        },
        {
          name: 'Tinte',
          price: 12000,
          min: true
        },
        {
          name: 'Depilación',
          price: 12000,
          min: true
        },
        {
          name: 'Maquillaje',
          price: 12000,
          min: true
        },
        {
          name: 'Limpieza facial',
          price: 12000
        },
        {
          name: 'Manicura',
          price: 12000
        },
        {
          name: 'Pedicura',
          price: 12000
        }
      ],
      dots:
        '....................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................'
    };
  }
};
</script>

<style scoped>
.container-fluid {
  background-color: #f6f6f6;
  padding: 60px 0px;
}
.title-container {
  text-align: center;
  padding-bottom: 40px;
}
.title-container div:first-child {
  font-size: 40px;
}
.title-container .title {
  font-size: 20px;
  font-weight: bold;
}

.price-container table {
  width: 80%;
  margin: 0 auto;
}
.price-container table tr td:first-child {
  overflow: hidden;
  white-space: nowrap;
  max-width: calc(60vw);
}
.price-container table tr td.value {
  width: 70px;
  text-align: right;
}
.price-container table tr td:last-child {
  width: 12px;
}
.note {
  text-align: center;
}
.note label:first-child {
  font-weight: bold;
}
</style>
