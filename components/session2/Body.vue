<template>
  <div>
    {{theme}}
    <Product :theme="theme"/>
    <Article :theme="theme"/>
  </div>
</template>

<script>
import Product from "./Product";
import Article from "./Article";
export default {
  components: {Article, Product},
  props: {
    theme: {
      type: Boolean,
      default: true
    }
  }
}
</script>
