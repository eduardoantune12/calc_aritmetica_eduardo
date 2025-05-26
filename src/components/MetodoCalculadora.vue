<script>
export default {
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