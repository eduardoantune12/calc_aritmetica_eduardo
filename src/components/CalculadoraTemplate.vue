<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-md-6 offset-md-3">
        <h1 class="text-center">Calculadora</h1>
        <form>
          <div class="form-group">
            <label for="numero1">Número 1:</label>
            <input type="number" class="form-control" id="numero1" v-model="numero1" @input="calcular" />
          </div>
          <div class="form-group">
            <label for="numero2">Número 2:</label>
            <input type="number" class="form-control" id="numero2" v-model="numero2" @input="calcular" />
          </div>
          <div class="form-group">
            <label for="operacao">Operação:</label>
            <select class="form-control" id="operacao" v-model="operacao" @change="calcular">
              <option value="+">Somar</option>
              <option value="-">Subtrair</option>
              <option value="*">Multiplicar</option>
              <option value="/">Dividir</option>
            </select>
          </div>
          <p class="text-center">Resultado: {{ resultado }}</p>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import CalculadoraLogic from './CalculadoraLogic.vue'

export default {
  mixins: [CalculadoraLogic]
}
</script>