<template>
  <div class="article">
    <Row>
      <h3>Articles</h3>
    </Row>
    <div class="article-item" v-for="item in articles" :key="item.name">
      <Row>
        <Column :sm="3">
          <img :src="item.img" alt="">
        </Column>
        <Column :sm="9" class="description">
          <h3>{{item.name}}</h3>
          <div class="mini">{{item.text}}</div>
        </Column>
      </Row>
    </div>
  </div>
</template>

<script>
import {getArticle} from "../../data/article";

export default  {
  data () {
    return {
      articles: []
    }
  },
  created() {
    getArticle({filter: {}, limit: 3})
      .then(data => {
        this.articles = data.data
        console.log(this.articles)
      })
  }
}
</script>
<style>
@import "assets/components/session2/style.scss";
</style>
