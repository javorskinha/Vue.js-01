
<template>
  <div>
    <Header :estaLogado="true"/>
    <PrimeiroComponente/>
    <p class="paragrafo-pai">O dado de app é {{ testando }}</p>
    <LifeCycle/>
    <Pessoa/>
  </div>
</template>

<script>
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'
  import Header from './components/Header.vue';
  export default{
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Header
    },
    data (){
      return{
        testando: "teste"
      }
    }
  }
</script>

<style>
  body{
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste{
    background-color: #000;
  }
</style>



