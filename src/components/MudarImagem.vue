<template>
    
    <div>
        <button @click="$emit('MudarImagem')">Trocar imagem de Perfil</button>
    </div>
</template>

<script>
export default{
    name: 'MudarImagem',
    emits: ['MudarImagem']
}
</script>