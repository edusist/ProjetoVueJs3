<template>
    <form action="">
      
        <div>
            <InputText/>
        </div>
        <div>
            <Enviar/>
        </div>
        </form>
</template>
<script>
import Enviar from './formulario/Enviar'
import InputText from './formulario/InputText';

export default{
    components: { 
        InputText,
        Enviar
    },
    name: 'FormEnvio'
}
</script>