<template>
<div class="container mt-5">
    <div class="row">
        <div class="col-md-6 offset-md-3">
            <div class="card">
                <div class="card-header">
                <h3>Calculadora</h3>
            </div>
                <div class="card-body">
                    <form>
                        <CampoEntrada
                            id="numero1"
                            label="Número 1"
                            v-model="numero1"
                        />
                        <CampoEntrada
                            id="numero2"
                            label="Número 2"
                            v-model="numero2"
                        />
                        <SelectOperacao
                            id="operacao"
                            v-model="operacao"
                        />
                        <p class="text-center">Resultado: {{ resultado }}</p>
                    </form>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import CampoEntrada from './CampoEntrada.vue'
import SelectOperacao from './SelectOperacao.vue'

export default {
    components: { CampoEntrada, SelectOperacao },
    props: {
    numero1: Number,
    numero2: Number,
    operacao: String,
    resultado: Number
    }
}
</script>