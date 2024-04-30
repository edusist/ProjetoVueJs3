<template>
    <div>
        <h2>Meu formulário:</h2>
        <form action="">
            <div>
                <InputText />
            </div>
            <div>
                <InputText />
            </div>
            <div>
                <Enviar />
            </div>
        </form>
    </div>
</template>

<script>
import Enviar from './formulario/Enviar'
import InputText from './formulario/InputText';

export default {
    components: {
        InputText,
        Enviar
    },
    name: 'FormEnvio'
}
</script>