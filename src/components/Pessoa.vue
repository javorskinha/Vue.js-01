<template>
    <div>
        <h2>Descrição de uma pessoa {{ nome }}</h2>
        <Info :email="email" :estaTrabalhando="true"/>
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
            nome: 'Matheus',
            email: 'blabla@email.com'
        }
    }
}
</script>



