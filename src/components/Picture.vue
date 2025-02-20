<template>
    <div>
        <MudarImagem @mudar-imagem="trocarImagem"/>
        <img :src="foto" alt="descricao">
    </div>
</template>

<script>
import MudarImagem from './MudarImagem.vue'
export default{
    name: 'Picture',
    components: { 
        MudarImagem
    },
    data (){
        return{
            foto: "../../public/favicon.ico",
            descricao: "minha foto"
        }
    },
    methods: {
        trocarImagem(){
            this.foto = "../../public/img/imagem.png"
        }
    }
}
</script>


