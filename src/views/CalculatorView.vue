<template>
    <div class="container text-center bg-success">
        <h1>Mi Primera Calculadora</h1>

    </div>
    <div class="position-relative vh-100">
        <Calculator></Calculator>
    </div>
</template>
<script>
import bootstrap from 'bootstrap/dist/js/bootstrap.bundle.js';//-
import Calculator from '../components/Calculator.vue';

export default {
    name: 'CalculatorView',
    components: {
        Calculator,
    },
    async mounted() {
        document.title = 'Calculator';
    },
}

</script>