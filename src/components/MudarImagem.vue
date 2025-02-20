<template>
    <div>
        <button @click="$emit('mudarImagem')">Trocar foto</button>
    </div>
</template>

<script>
    export default {
        name: 'MudarImagem',
        emits: ['mudarImagem']
    }
</script>




