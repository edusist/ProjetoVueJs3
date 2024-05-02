<template>
    <div>
        <h2>Meu formulário:</h2>
        <form action="" @submit="enviarFormulario($event)">
            <div>
               <input type="text" name="" id="" v-model="name">
            </div>
            <div>
                <input type="email" name="" id="" v-model="email">
            </div>
            <div>
                <Enviar />
            </div>
        </form>
        <p>Conteúdo</p>
        <p>Conteúdo</p>
        <p>Conteúdo</p>
    </div>
</template>

<script>
import Enviar from './formulario/Enviar'
// import InputText from './formulario/InputText';

export default {
    name: 'FormEnvio',
    components: {
        // InputText,
        Enviar
    },
    data(){
        return {
            name: '',
            email: ''
        }
    },

    methods: {
        enviarFormulario(e) {

            e.preventDefault();
            
            const name = this.name;
            const email = this.email;
            console.log('O Nome é '+ name);
            console.log('O E-mail é '+ email);

            //Ajax
            //Inserir no banco dados 
        }
    }
}
</script>

<style>
p{
    margin:150px;
}
</style>