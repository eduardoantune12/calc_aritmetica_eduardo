<template>
<div>
    <CorpoCalculadora
        :numero1="numero1"
        :numero2="numero2"
        :operacao="operacao"
        :resultado="resultado"
        @update:numero1="updateNumero1"
        @update:numero2="updateNumero2"
        @update:operacao="updateOperacao"
    />
</div>
</template>

<script>
import CorpoCalculadora from './CorpoCalculadora.vue'
import DadosCalculadora from './DadosCalculadora.vue'
import MetodosCalculadora from './MetodosCalculadora.vue'

export default {
    components: { CorpoCalculadora },
    mixins: [DadosCalculadora, MetodosCalculadora]
}
</script>