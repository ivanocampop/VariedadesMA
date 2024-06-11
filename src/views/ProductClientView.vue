<template>
    <div>
        <Nav></Nav>
        <div>
            <ProductClient></ProductClient>
        </div>

    </div>
</template>
<script>
import bootstrap from 'bootstrap/dist/js/bootstrap.bundle.js';//-
import Nav from '../components/Nav.vue';
import ProductClient from '../components/ProductClient.vue';


export default {
    name: 'ProductClientView',
    components: {
        ProductClient,
        Nav
    },
    async mounted() {
        document.title = 'ProductClient';
    },
}

</script>