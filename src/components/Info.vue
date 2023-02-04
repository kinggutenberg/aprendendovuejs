<template>
    <div>
        <p>{{ compEmail }} - {{ email }}</p>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>estou em busca de uma oportunidade</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul >
            <li v-for="(technology, index) in backend_techologies" v-bind:key="index"> {{ technology }} </li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front end:</p>
        <ul >
            <li v-for="technology in frontend_techologies" :key="technology.id"> {{ technology.language }} </li>
        </ul>
        <div>
            <button @click="showEmail"> {{ textoBotao }} </button>
        </div>
        <p v-show="mostrar_email">Manda uma mensagem para {{ email }} </p>
        <p>Para acessar meu portifolio <a v-bind:href="meu_link" target="_blank">clicar aqui</a></p>
        <Picture />
    </div>
    
</template>
<script>
import Picture from './Picture.vue'
export default {
    name: 'Info',
    components: {
        Picture,
    },
    props: {
        email: String
    },
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: false,
            meu_link: 'https://kinggutenberg.github.io/',
            textoBotao: "mostrar email",
            backend_techologies: ['JS', 'PHP', 'python'],
            frontend_techologies: [
                {id: 1, language: "HTML"},
                {id: 2, language: "CSS"},
                {id: 3,language: "cobol"}
            ]
        }
    },
    methods: {
       showEmail() {
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email){
            this.textoBotao = 'Mostrar e-mail'
        } else{
            this.textoBotao = 'esconder e-mail'
        }
       } 
    }
}
</script>
