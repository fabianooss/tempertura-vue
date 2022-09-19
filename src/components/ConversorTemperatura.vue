<template>
  <div>
    <h1>Temperatura</h1>
    <table>
      <tr>
        <th>Celsius</th>
        <th>Farenheight</th>
      </tr>  
      <tr v-for="t in temperatura" :key="t.celsius">
        <td>{{t.celsius}}</td>
        <td>{{t.farenheight}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    temperturaInicial: Number,
    temperaturaFinal: Number
  },
  data() {
    return {
      temperatura: []
    }
  },
  mounted() {
    this.calcularTemperatura()
  },
  methods: {
    calcularTemperatura() {
       for (let i = this.temperturaInicial; i <= this.temperaturaFinal; i++)  {
          this.temperatura.push({
             celsius: i,
             farenheight: (i * 9 / 5)  + 32
          }) 
       }
    }
  }

}
</script>

<style>

</style>