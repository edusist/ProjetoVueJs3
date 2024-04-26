<template>
    <div>
        <primeiroComponente /> 
        <p>O dado de app é: {{ testando }}</p>
        <LifeCycle/>
        <Pessoa/>
    </div>
 
</template>

<script>

//Tem que importar do componente e disser de onde está sendo importado e patch
import primeiroComponente from './components/primeiroComponente.vue';
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';

//Necessario o exportar, para arquivo main.js saber que este e arquivo App.vue
export default{
    name: 'App',
    //Necessário dizer para Vue que vou utilizar um componente 
    components: {
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