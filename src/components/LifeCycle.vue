<template>
    <h1>Meu nome é {{ nome }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data(){
        return {
            nome: 'sem nome'
        }
    },
    created (){
        setTimeout(() => {
            this.nome = 'Matheus'
        }, 1000);

        this.lifeCycle()
    },
    mounted () {
        setTimeout(() => {
            this.nome = 'Pedro'
        }, 2000)

        this.lifeCycle()
    },
    methods: {
        lifeCycle(){
            console.log("executou")
        }
    }
}
</script>


