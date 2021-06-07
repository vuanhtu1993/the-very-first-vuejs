<template>
  <div>
    <Row justify="start">
      <nuxt-link :to="'session2/'" style="margin-right: 1rem">Home</nuxt-link>
      <hr style="margin-right: 1rem">
      <nuxt-link :to="'session2/articles'" style="margin-right: 1rem">Articles</nuxt-link>
      <hr style="margin-right: 1rem">
      <nuxt-link :to="'session2/products'" style="margin-right: 1rem">Products</nuxt-link>
    </Row>
    <hr>
  </div>
</template>

<script>
export default {

}
</script>
<style lang="scss" scoped>
@import "assets/components/session2/style.scss";
</style>
