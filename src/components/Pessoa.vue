<template>
    <div>
        <h2>Descrição de uma pessoa {{ nome }}</h2>
        <Info />
    </div>
</template>

<script>
import Info from './Info.vue'
export default {
    name: 'Pessoa',
    components: {
        Info
    },
    data () {
        return {
            nome: 'Matheus'
        }
    }
}
</script>



