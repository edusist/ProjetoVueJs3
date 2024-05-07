<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <!-- Está chamando o método no componente MudarImagem.vue -->
        <MudarImagem @mudar-imagem="TrocarImagem" />
    </div>
</template>

<script>
import MudarImagem from './MudarImagem.vue';
// import Reutilizacao from './Reutilizacao.vue'
export default {
    components: {
        MudarImagem
    },
    name: 'Picture',
    data() {
        return {
            avatar: '/img/avatar.png',
            descricao: 'Eduardo Augusto'
        }
    },
    methods:{
        TrocarImagem(){
            this.avatar = '/img/avatar2.png'
        }
    }
}

</script>