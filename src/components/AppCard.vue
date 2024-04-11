<template>
    <div class="card">
        <div class="img-box">
            <img :src="`/src/assets/img/${product.frontImage}`" alt="modello per abbigliamento">
            <img :src="`/src/assets/img/${product.backImage}`" alt="modello per abbigliamento">
            <span v-if="product.isInFavorites" class="favorite">&hearts;</span>
            <span v-else="product.isInFavorites" class="favorite">&#9825;</span>
            <div class="badge">
                <span v-for="badge in product.badges" :class="badge.type"> {{ badge.value }} </span>
            </div>
        </div>
        <h3 class="brand"> {{ product.brand }} </h3>
        <h2 class="description"> {{ product.name.toUpperCase() }} </h2>
        <span class="price-box">
            <p class="price">{{ product.price }} &euro;</p>
            <s class="price-discounted">{{ product.price }} &euro;</s>
        </span>
    </div>
</template>
<script>
export default {
    props: ['product'],
}
</script>

<style lang="scss" scoped>
.badge {
    .discount {
        background-color: red;
    }

    .tag {
        background-color: green;
    }
}
</style>