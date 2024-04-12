<template>
    <section class="container">
        <div class="row">

            <app-card v-for="(product, i) in products" :product="product" :key="i" />

        </div>
    </section>
</template>
<script>
import { store } from '../store.js';

import AppCard from "./AppCard.vue";
// import dbProducts from "../assets/db.json";
export default {
    components: { AppCard },
    data() {
        return {
            products: store.products
        }
    },
    mounted() {
        console.log(this.products);
    }
}
</script>

<style lang="scss" scoped></style>