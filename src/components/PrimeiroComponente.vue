<template>
    <div>
        <h1>Olá Mundo!</h1>
        <p>Meu nome é {{ nome }} e estudo {{ estudo }}</p>
        <MultiplosEventos />
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos
        },
        data () {
            return{
                nome: "Andrieli", 
                estudo: "programação"
            }
        }
    }
</script>

