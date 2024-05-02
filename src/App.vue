<template>
    <div>
        <HeaderApp :esta_logado='true' />
        <primeiroComponente /> 
        <p class="paragrafo-pai">O dado de app é: {{ testando }}</p>
        <LifeCycle/>
        <Pessoa/>
    </div>
 
</template>

<script>

//Tem que importar do componente e disser de onde está sendo importado e patch
import HeaderApp from './components/HeaderApp.vue';
import primeiroComponente from './components/primeiroComponente.vue';
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';

//Necessario o exportar, para arquivo main.js saber que este e arquivo App.vue
export default{
    name: 'App',
    //Necessário dizer para Vue que vou utilizar um componente 
    components: {
        HeaderApp,
        primeiroComponente,
        LifeCycle,
        Pessoa
       
    },
    data(){
        return {
            testando: 'teste'
        }
    }
}
</script>
<style>
body{
    background-color: #333;
    color: #fff;
}
a{
    color: red;
}
.teste{
    background-color: #000;
}
</style>