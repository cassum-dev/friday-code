<template>
  <div class="list-container">
    <div v-for="product in products" :key="product.id" class="product-card">
      <div>
        <img :src="require('./../assets/' + product.image)">

        <div>
            <h4>{{ product.name }}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Products from './../data-sources/product-list.json';

export default {
  name: 'ProductList',
  data () {
    return {
      products: Products.products,
    }
  }
}
</script>

<style scoped>
a {
  color: #35495e;
  text-decoration: none;
}

.list-container {
  margin-left: 15%;
  margin-right: 15%;
  display: flex;
  flex-flow: row wrap;
  justify-content: flex-start;
}

.product-card {
  flex-basis: 24%;
}

.product-card:hover {
  flex-basis: 25%;
  cursor: pointer;
}
</style>
