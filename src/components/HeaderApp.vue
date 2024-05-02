<template>
    <ul>
        <li> <a href="http://" target="_blank"></a>Home</li>
        <li> <a href="http://" target="_blank"></a>Projetos</li>
        <li> <a href="http://" target="_blank"></a>Contato</li>
        <li v-if="esta_logado"><a href="#">Meu Perfil</a></li>    
    </ul>
</template>

<script>
export default {
    name: 'HeaderApp',
    props: ['esta_logado']

}
</script>
<!-- Este estilo somente para este componente -->
<style scoped>
    ul{
        list-style: none;
        display: flex;
        background-color: #000;
    }   
    li{
        margin-right: 10px;
    }

    a{
        color: #ddd;
        text-decoration: none;
        transition: .5s;
    }

    a:hover{
        color: turquoise;
    }
</style>
