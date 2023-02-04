<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        <Info :email="email"/>
    </div>
</template>

<script>
    import Info from './Info'

    export default {
        name: 'Pessoa',
        components: {
           Info,
        },
        data(){
            return {
                nome: 'Matheus',
                email: 'douglasgutenberg3@gmail.com'

            }
        }
    }
</script>