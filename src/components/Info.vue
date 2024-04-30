<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias</p>
        <ul>
            <li>JavaScript</li>
            <li>Php</li>
            <li>Python</li>
        </ul>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ mail }}</p>
        <!-- Para o link ser dinâmico e Necessario ter a diretiva v-bind -->
        <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">Basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue'
export default {
    components: {
        Picture
    },
    name: 'Info',
    data(){
         return{
            esta_trabalhando: false,
            mostrar_email: false,
            mail: 'eduardo@mail.com',
            meu_link: 'https://google.com'
         }
    }
}
</script>