<template>
    <div>
        <conversor-temperatura 
            :temperturaInicial="1"
            :temperaturaFinal="100" >

        </conversor-temperatura>
    </div>
</template>

<script>
import ConversorTemperatura from './components/ConversorTemperatura.vue'
export default {
  components: {
    ConversorTemperatura
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 60px;
  border: 1px solid silver;
  padding: 20px 5px 5px 20px;

}
</style>
