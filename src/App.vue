<template>
  <header>
    <cmp-header />
  </header>
  <main>
    <cmp-main />
  </main>
  <footer>
    <cmp-footer />
  </footer>

</template>

<script>
import { store } from './store.js';
import axios from 'axios';

import CmpHeader from './components/CmpHeader.vue'
import CmpMain from './components/CmpMain.vue'
import CmpFooter from './components/CmpFooter.vue'


export default {
  components: { CmpHeader, CmpMain, CmpFooter },
  // data(){
  //   return{
  //     store : store 
  //   }
  // },
  
  // }
  created() {
    axios.get('http://localhost:3000/products').then((res) => {
      store.products = res.data
    })
    console.log('--');
  
  }
}
</script>

<style lang="scss">
@use './styles/general';

header {
  background-color: rgb(255, 105, 0);
}

footer {
  background-color: #1A1A1A;
  color: white;
  padding: 20px 0;
  font-size: 0.7em;
}
</style>
