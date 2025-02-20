<template>
    <div>
        <p v-if="estaTrabalhando">Estou trabalhando no momento.</p>
        <p v-else>Não estou trabalhando no momento</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for="(technology, index) in backendtTechnologies" :key="index">{{ technology }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in frontendTechnologies" :key="technology.id">{{ technology.language }}</li>
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
            textoBotao: 'Mostrar email',
            backendtTechnologies: ['Javascript', 'PHP', 'Python', 'Node.js', 'Laravel'],
            frontendTechnologies: [
                {id:1, language: 'HTML'},
                {id:2, language: 'CSS'},
                {id:3, language: 'Javascript'}
            ]
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

<style>
    .paragrafo-pai{
        color: red;
    }
</style>



