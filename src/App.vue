<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue';
export default{
  name: 'App',
  components: {PrimeiroComponente},
  data (){
    return{
      testando: "teste"
    }
  }
}
</script>

<template>
  <div>
    <PrimeiroComponente/>
    <p>O dado de app é {{ testando }}</p>
  </div>
</template>


<style scoped>
</style>



