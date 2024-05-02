<template>
    <div>
        <button @click="primeiro(txt, $event), segundo(txt2, $event), terceiro()">Ativar multiplos Eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
export default{
    name: 'MultiplosEventos',
    data(){
        return {
            multiplos_eventos: '',
            txt: 'Primeiro Evento',
            txt2: 'Segundo Evento'
        }
    },
    methods: {
        primeiro(txt, e){
            this.multiplos_eventos = txt;
        },
        segundo(txt, e){
            setTimeout(() => this.multiplos_eventos = txt, 1000)
        },
        terceiro(){
            setTimeout(()=> this.multiplos_eventos = '', 1500)
        }
    }
}
</script>

 <style scoped>
div{

    margin: 100px;
}
</style>