<template>
    <img :src="foto" alt="descricao">
</template>

<script>
export default{
    name: 'Picture',
    data (){
        return{
            foto: "../../public/favicon.ico",
            descricao: "minha foto"
        }
    }
}
</script>


