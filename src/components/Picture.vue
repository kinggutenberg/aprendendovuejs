<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <mudarimagem @mudar-imagem="Trocarimagem"/>
    </div>
</template>
<script>
import MudarImagem from "./Mudarimagem.vue"

export default{
    name: 'Picture',
    components: {
        MudarImagem

    },
    data() {
        return {
            avatar: "/img/euicon.png",
            descricao: "Douglas Gutenberg"
        }
    },
    methods: {
        Trocarimagem(){
            console.log(opa)

        }
    }
}
</script>