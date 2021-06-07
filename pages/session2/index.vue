<template>
  <div class="session2-container">
    <Header/>
    <Row right>
      <button @click="changeTheme()">Change theme</button>
    </Row>
    <Title/>
    <Body :theme="theme"/>
    <Footer/>
  </div>
</template>

<script>
import Header from "../../components/session2/Header";
import Title from "../../components/session2/Title";
import Body from "../../components/session2/Body";
import Footer from "../../components/session2/Footer";
export default {
  components: {
    Footer,
    Body,
    Title,
    Header
  },
  data() {
    return {
      theme: true
    }
  },
  methods: {
    changeTheme() {
      this.theme = !this.theme
    }
  }
}
</script>

<style>
@import "assets/components/session2/style.scss";
</style>
