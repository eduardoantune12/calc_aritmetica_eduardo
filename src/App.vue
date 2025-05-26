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
              <div class="form-group">
                <label for="numero1">Número 1</label>
                <input type="number" class="form-control" id="numero1" v-model="numero1" placeholder="Número 1">
              </div>
              <div class="form-group">
                <label for="numero2">Número 2</label>
                <input type="number" class="form-control" id="numero2" v-model="numero2" placeholder="Número 2">
              </div>
              <div class="form-group">
                <label for="operacao">Operação</label>
                <select class="form-control" id="operacao" v-model="operacao">
                  <option value="+">Soma</option>
                  <option value="-">Subtração</option>
                  <option value="*">Multiplicação</option>
                  <option value="/">Divisão</option>
                </select>
              </div>
              <p class="text-center">Resultado: {{ resultado }}</p>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: '+',
      resultado: 0
    }
  },
  watch: {
    numero1() {
      this.calcular()
    },
    numero2() {
      this.calcular()
    },
    operacao() {
      this.calcular()
    }
  },
  methods: {
    calcular() {
      switch (this.operacao) {
        case '+':
          this.resultado = this.numero1 + this.numero2
          break
        case '-':
          this.resultado = this.numero1 - this.numero2
          break
        case '*':
          this.resultado = this.numero1 * this.numero2
          break
        case '/':
          this.resultado = this.numero1 / this.numero2
          break
      }
    }
  }
}
</script>