<template>
  <div class="product">
    <Row>
      <h3>Products</h3>
    </Row>
    <Row>
      <Column class="product-item" v-for="item in products" :key="item.name" :sm="12" :md="4">
        <img :src="item.img" alt="">
        <div>{{item.name}}</div>
        <div>{{item.price}}</div>
        {{theme}}
      </Column>
    </Row>
  </div>
</template>

<script>
import {getProduct} from "../../data/product";

export default  {
  props: {
    theme: {
      type: Boolean,
      default: true
    }
  },
  data () {
    return {
      products: []
    }
  },
  created() {
    getProduct({filter: {}, limit: 3})
    .then(data => {
      this.products = data.data
      console.log(this.products)
    })
  }
}
</script>

<style>
@import "assets/components/session2/style.scss";
</style>
