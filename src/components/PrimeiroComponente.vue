<template>
    <div>
        <Reutilizacao />
        <h1>Olá Mundo!</h1>
        <Reutilizacao />
        <p>Meu nome é {{ nome }} e estudo {{ estudo }}</p>
        <MultiplosEventos />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue';
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data () {
            return{
                nome: "Andrieli", 
                estudo: "programação"
            }
        }
    }
</script>

