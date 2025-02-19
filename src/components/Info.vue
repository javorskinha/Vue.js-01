<template>
    <div>
        <p v-if="estaTrabalhando">Estou trabalhando no momento.</p>
        <p v-else>Não estou trabalhando no momento</p>
        <p>Utilizo as tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
            <li>Python</li>
        </ul>
        <Form />
        <p v-if="4>2">TESTANDO</p>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrarEmail">mande uma mensagem para {{ email }}</p>
        <p class="teste">Para acessar meu portifolio basta <a v-bind:href="meuLink" target="_blank">acessar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Form from './Form.vue'
import Picture from './Picture.vue';
export default{
    name: 'Info',
    components: {
        Form,
        Picture
    },
    data (){
        return{
            estaTrabalhando: true,
            mostrarEmail: false,
            email: 'andri@gmail.com',
            meuLink: 'https://google.com',
            textoBotao: 'Mostrar email'
        }
    },
    methods: {
        showEmail(){
            this.mostrarEmail = !this.mostrarEmail
            if(!this.mostrarEmail){
                this.textoBotao = 'Mostrar email'
            } else {
                this.textoBotao = 'Esconder email'
            }
        }
    }
}
</script>




