<template>
    <h1>meu nome é: {{ nome }}</h1>
</template>

<script>
export default{
    name: 'LyfeCycle',
    data() {
        return {
            nome: 'Ainda não sei'
        }
    },
    created() {
        setTimeout(() =>{
        this.nome = 'Matheus'
        }, 1000);
    },
    mounted() {
        setTimeout(() =>{
        this.nome = 'Douglas'    
        }, 2000);
    },
    methods: {
        lifeCycle() {
            console.log("Executou");
        }
    }
}
</script>
