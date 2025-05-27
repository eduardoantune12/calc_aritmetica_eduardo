<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: "+",
      resultado: 0
    }
  },
  methods: {
    calcular() {
      const num1 = parseFloat(this.numero1)
      const num2 = parseFloat(this.numero2)
      switch (this.operacao) {
        case "+":
          this.resultado = num1 + num2
          break
        case "-":
          this.resultado = num1 - num2
          break
        case "*":
          this.resultado = num1 * num2
          break
        case "/":
          this.resultado = num1 / num2
          break
      }
    }
  }
}
</script>
