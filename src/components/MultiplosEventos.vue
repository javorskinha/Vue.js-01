<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro($event)">Ativar múltiplos eventos</button>
        <p>{{ multiplosEventos }}</p>
    </div>
</template>

<script>
    export default {
        name: 'MultiplosEventos',
        data (){
        return {
            multiplosEventos: "",
            txt1: "Primeiro evento ativado",
            txt2: "Segundo evento ativado"
        }
        },
        methods: {
            primeiro(e) {
                this.multiplosEventos = this.txt1;
            },
            segundo(e) {
                setTimeout(() => this.multiplosEventos = this.txt2, 500)
            },
            terceiro(e) {
                setTimeout(() => this.multiplosEventos = "", 1500)
            }
        }
    }
</script>




