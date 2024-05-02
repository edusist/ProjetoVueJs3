<template>
    <div>
        <h2>Está é a descrição da pessoa: {{ nome }}</h2>
        <Info :email='email' :esta_trabalhando='true' />
     <FormEnvio />
    </div>
</template>

<script>

import Info from './Info'
import FormEnvio from './FormEnvio';

export default {
    
    name: 'Pessoa',
    //Este Componente dependá de outros componentes
    components:{
    Info,
    FormEnvio
},  
    data() {
        return {
            nome: 'Eduardo',
            email: 'eduardo@mail.com'
        };
    }
}
</script>