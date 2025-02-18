<script>
    export default {
        name: 'PrimeiroComponente',
        data () {
            return{
                nome: "Andrieli", 
                estudo: "programação"
            }
        }
    }
</script>

<template>
    <div>
        <h1>Olá Mundo!</h1>
        <p>Meu nome é {{ nome }} e estudo programação</p>
    </div>
</template>


