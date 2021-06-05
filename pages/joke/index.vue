<template>
  <div class="container">
    <Header/>
    <div class="body">
        <div class="joke-item" v-for="item in data">
          <nuxt-link v-bind:to="'joke/' + item.id">
            <div>{{item.joke}}</div>
            <div>{{item.id}}</div>
          </nuxt-link>
        </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Header from "../../components/common/Header";

export default {
  components: {Header},
  data() {
    return {
      data: [],
    }
  },
  async created() {
    await this.fetchJokes()
  },
  methods: {
    async fetchJokes() {
      const config = {
        headers: {
          'Accept': "application/json"
        }
      }
      try {
        const response = await axios.get('https://icanhazdadjoke.com/search', config)
        this.data = response.data.results
        console.log(response)
      }
      catch (err) {
        console.log(err)
      }
    }
  }
}
</script>
<style lang="scss" scoped>
@import "assets/components/joke.scss";
</style>
