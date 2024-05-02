<template>
    <div>
        <!-- <p>- {{ email = 'eduardo@mail.com' }}</p>  -->
        <!-- {{ Email }}  -->
        <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias para Back-end:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
                {{ technology }}
            </li>      
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id">           
            {{ technology.language }}
            </li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <!-- Para o link ser dinâmico e Necessario ter a diretiva v-bind -->
        <p class="teste">Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">Basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue'
export default {
    components: {
        Picture
    },
    props:{
        email: String,
        esta_trabalhando: Boolean
    },
    name: 'Info',
    data(){
         return{
            // esta_trabalhando: false,
            mostrar_email: false,
            // email: 'eduardo@mail.com',
            meu_link: 'https://google.com',
            textoBotao: 'Mostrar E-mail',
            backend_technologies:['JavaScript', 'Php','Python'],
            frontend_technologies:[
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'VUE'}
            ]
         }
    },
    methods:{
        showEmail(){
            //Mostra o contrário do boleano
            this.mostrar_email = !this.mostrar_email
            
            //Inverter o boleando Se for true vira false
            if (!this.mostrar_email) {
                this.textoBotao = 'Mostrar E-mail'
            }else{
                this.textoBotao = 'Esconder E-mail'
            }
        }
    }
}
</script>
<style>
.paragrafo-pai{
    color: red;
}
</style>