<template>
    <div class="container w-50">
        <div class="row">
            <div class="col-12">
                <input type="text" class="form-control text-end fw-bold fs-3" v-model="resultado">
            </div>
            <div class="col-12">
                <div class="row">
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6">AC</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6" @click="reset">C</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6">%</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6" @click="division">/</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('7')">7</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('8')">8</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('9')">9</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6" @click="multiplicacion">*
                        </botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('4')">4</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('5')">5</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('6')">6</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6" @click="resta">-</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('1')">1</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('2')">2</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('3')">3</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6" @click="suma">+</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('00')">00</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-light my-2 form-control fw-bold fs-6" @click="boton('0')">0</botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-secondary my-2 form-control fw-bold fs-6" @click="botonDecimal">.
                        </botton>
                    </div>
                    <div class="col-3">
                        <botton class="btn btn-success my-2 form-control fw-bold fs-6" @click="igual">=</botton>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Calculator',
    data() {
        return {
            resultado: '0',
            valor: 0,
            prepararValorSuma: false,
            prepararValorResta: false,
            prepararValorMultiplica: false,
            prepararValorDividir: false,
            operador: null,
        }
    },
    methods: {
        boton(numeroCadena) {
            console.log('clic en num', this.resultado, this.operador, this.valor)
            console.log(this.prepararValorSuma, this.prepararValorResta, this.prepararValorMultiplica, this.prepararValorDividir);

            if (this.valor > 0) {
                console.log('ASDASDASDASF');
                switch (this.operador) {
                    case '+':
                        this.resultado = numeroCadena
                        if (!this.prepararValorSuma) {
                            this.prepararValorSuma = true
                        }
                        break
                    case '-':
                        if (!this.prepararValorResta) {
                            this.prepararValorResta = true
                        }
                        break
                    case '*':
                        if (!this.prepararValorMultiplica) {
                            this.prepararValorMultiplica = true
                        }
                        break
                    case '/':
                        if (!this.prepararValorDividir) {
                            this.prepararValorDividir = true
                        }
                        break
                }
            } else if (this.resultado === '0' && numeroCadena != '00') {
                this.resultado = numeroCadena
            } else if (this.resultado != '0') {
                this.resultado = this.resultado + numeroCadena
            }
            console.log(this.prepararValorSuma, this.prepararValorResta, this.prepararValorMultiplica, this.prepararValorDividir);
        },
        botonDecimal() {
            if (this.esperandoNuevoValor) {
                this.resultado = '0.'
                this.esperandoNuevoValor = false
            } else if (!this.resultado.includes('.')) {
                this.resultado += '.'
            }
        },
        suma() {
            console.log('clic en suma', this.resultado, this.operador, this.valor)
            console.log(this.prepararValorSuma, this.prepararValorResta, this.prepararValorMultiplica, this.prepararValorDividir);

            switch (this.operador) {
                case '+':
                    if (this.prepararValorSuma) {
                        this.valor = this.valor + parseFloat(this.resultado)
                        console.log(this.valor, parseFloat(this.resultado));
                        this.resultado = String(this.valor)
                        this.prepararValorSuma = false
                    }
                    break
                case '-':
                    if (this.prepararValorResta) {
                        this.valor = this.valor - parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorResta = false
                    } 
                    break
                case '*':
                    if (this.prepararValorMultiplica) {
                        this.valor = this.valor * parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorMultiplica = false
                    } 
                    break
                case '/':
                    if (this.prepararValorDividir) {
                        this.valor = this.valor / parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorDividir = false
                    } 
                    break
            }
            this.valor = parseFloat(this.resultado)
            this.operador = '+'
            console.log(this.operador, 'operador');

        },
        resta() {
            console.log('clic en resta', this.resultado)
            console.log(this.prepararValorSuma, this.prepararValorResta, this.prepararValorMultiplica, this.prepararValorDividir);

            switch (this.operador) {
                case '+':
                    if (this.prepararValorSuma) {
                        this.valor = this.valor + parseFloat(this.resultado)
                        console.log(this.valor, parseFloat(this.resultado));
                        this.resultado = String(this.valor)
                        this.prepararValorSuma = false
                    }
                    break
                case '-':
                    if (this.prepararValorResta) {
                        this.valor = this.valor - parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorResta = false
                    } 
                    break
                case '*':
                    if (this.prepararValorMultiplica) {
                        this.valor = this.valor * parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorMultiplica = false
                    } 
                    break
                case '/':
                    if (this.prepararValorDividir) {
                        this.valor = this.valor / parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorDividir = false
                    } 
                    break
            }
            this.valor = parseFloat(this.resultado)
            this.operador = '-'
            console.log(this.operador, 'operador');

        },
        multiplicacion() {
            console.log('clic en multiplicacion', this.valor)
            console.log(this.prepararValorSuma, this.prepararValorResta, this.prepararValorMultiplica, this.prepararValorDividir);

            switch (this.operador) {
                case '+':
                    if (this.prepararValorSuma) {
                        this.valor = this.valor + parseFloat(this.resultado)
                        console.log(this.valor, parseFloat(this.resultado));
                        this.resultado = String(this.valor)
                        this.prepararValorSuma = false
                    }
                    break
                case '-':
                    if (this.prepararValorResta) {
                        this.valor = this.valor - parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorResta = false
                    } 
                    break
                case '*':
                    if (this.prepararValorMultiplica) {
                        this.valor = this.valor * parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorMultiplica = false
                    } 
                    break
                case '/':
                    if (this.prepararValorDividir) {
                        this.valor = this.valor / parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorDividir = false
                    } 
                    break
            }
            this.valor = parseFloat(this.resultado)
            this.operador = '*'
            console.log(this.operador, 'operador');
        },
        division() {
            console.log('clic en division', this.valor)

            switch (this.operador) {
                case '+':
                    if (this.prepararValorSuma) {
                        this.valor = this.valor + parseFloat(this.resultado)
                        console.log(this.valor, parseFloat(this.resultado));
                        this.resultado = String(this.valor)
                        this.prepararValorSuma = false
                    }
                    break
                case '-':
                    if (this.prepararValorResta) {
                        this.valor = this.valor - parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorResta = false
                    } 
                    break
                case '*':
                    if (this.prepararValorMultiplica) {
                        this.valor = this.valor * parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorMultiplica = false
                    } 
                    break
                case '/':
                    if (this.prepararValorDividir) {
                        this.valor = this.valor / parseFloat(this.resultado)
                        console.log(this.valor);
                        this.resultado = String(this.valor)
                        this.prepararValorDividir = false
                    } 
                    break
            }
            this.valor = parseFloat(this.resultado)
            this.operador = '/'
            console.log(this.operador, 'operador');

        },
    }
}
</script>