<template>
    <ul>
        <li><a href="#">home</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Contato</a></li>
    </ul>
    
</template>
<script>
  export default{
    name: 'Header'
}
</script>
<style scoped>
ul {
    list-style: none;
    display: flex;
    background-color: #ccc;
}
li{
    margin-right: 10px;
}
a{
    color: #ddd;  
    text-decoration: none;
    transition: .4s;
}
a:hover{
    color: turquoise;
}
</style>
