<template>
 
        <h1>Meu nome é: {{ nome }}</h1>
   
</template>

<script>

export default{
    name: 'LifeCycle',
    data() {
        return{
            nome: 'Qualquer coisa'
        }
     
    },
    // Eventos acontecendo em determinada etapa da minha aplicação
    created(){

        setTimeout(() => {
            this.nome= 'Eduardo'
        }, 1000);        
          
        },
    mounted(){
        
        setTimeout(() => {
            this.nome = 'Pedro'
        }, 2000);
   
    }

}
</script>