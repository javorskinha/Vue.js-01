<template>
    <form action="" @submit="enviarFormulario($event)">
        <input type="text" v-model="name"><br>
        <input type="text" v-model="email"><br>
        <Submit/>
    </form>
</template>

<script>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'
export default{
    name: 'Form',
    components: {
        InputText,
        Submit
    },
    data(){
        return{
            name: "",
            email: ""
        }
    },
    methods: {
        enviarFormulario(e){

            e.preventDefault();

            const name = this.name;
            const email = this.email;

            console.log("formulario enviado");
            console.log("o nome é " + name);
            console.log("o email é " + email)

            //ajax

            //inserir os dados no banco
        }
    }
}
</script>




