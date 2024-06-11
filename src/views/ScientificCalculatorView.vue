<template>
    <div class="container text-center bg-secondary mt-2">
        <h1>Mi Primera Calculadora cientifica</h1>
    </div>
    <div class="position-relative">
        <ScientificCalculator></ScientificCalculator>
    </div>
</template>
<script>
import bootstrap from 'bootstrap/dist/js/bootstrap.bundle.js';//-
import ScientificCalculator from '../components/ScientificCalculator.vue';

export default {
    name: 'ScientificCalculatorView',
    components: {
        ScientificCalculator,
    },
    async mounted() {
        document.title = 'ScientificCalculator';
    },
}
</script>