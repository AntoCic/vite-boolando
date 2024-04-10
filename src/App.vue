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
import CmpHeader from './components/CmpHeader.vue'
import CmpMain from './components/CmpMain.vue'
import CmpFooter from './components/CmpFooter.vue'

export default {
  components: { CmpHeader, CmpMain, CmpFooter },
  data() {
    return {
      titolo: "TITOLO"
    }
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
