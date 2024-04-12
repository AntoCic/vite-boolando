<template>
    <nav class="container">
        <div class="row align-items-center">
            <div class="col-4">
                <a href="#">Donna</a>
                <a href="#">Uomo</a>
                <a href="#">Bambini</a>
            </div>
            <div class="col-4 text-center">
                <img  @click="console.log(store.products)" src="../assets/img/boolean-logo.png" alt="logo">
            </div>
            <div class="col-4 text-end">
                <button>U</button>
                <button>F</button>
                <button>C</button>
            </div>
        </div>
    </nav>
</template>

<script>
import { store } from '../store.js';


export default {
  data(){
    return{
        store : store
    }
  }
}
</script>

<style lang="scss" scoped>
img {
    display: inline-block;
    width: 100px;
    margin: 10px 0;
}

a {
    font-size: 0.8em;
    display: inline-block;
    color: white;
    margin-left: 12px;
    &:first-child{margin-left: 0;}
}

button {
    display: inline-block;
    color: white;
    border: 0;
    background-color: transparent;
    padding: 3px 5px;
}

</style>