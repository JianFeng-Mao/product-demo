<template>
  <div id="app">
    <ProductList />
  </div>
</template>

<script>
import ProductList from './components/ProductList.vue'

export default {
  name: 'App',
  components: {
    ProductList
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

ul,
li {
  list-style: none;
}
</style>
