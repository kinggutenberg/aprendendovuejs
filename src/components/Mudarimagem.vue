<template>
    <div>
        <button @click="$emit('mudarimagem')">trocar imagem </button>
    </div>
</template>
<script>
export default{
    name: 'MudarImagem',
    emits: ['mudarImagem']
}
</script>
