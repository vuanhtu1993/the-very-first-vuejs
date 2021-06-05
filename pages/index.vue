<template>
  <div class="wrapper">
    <div class="header">
      <div>
        <Logo />
        <h4 class="title">
          <Parent/>
        </h4>
      </div>
    </div>
    <div class="body">
      <h3>Dad Jokes</h3>
      <div class="joke">
        <nuxt-link :to="'/joke'"></nuxt-link>
      </div>
      <h3>Understanding props and state</h3>
      <Games/>
    </div>
  </div>
</template>

<script>
import Parent from "../components/learnComponent/Parent";
import Games from "../components/propsAndState/Games";
export default {
  components: {
    Games,
    Parent
  }
}
</script>

<style>
.header {
  margin: 0 auto;
  /*Separate with fullpage header and only full page*/
  /*min-height: 100vh;*/
  height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.joke {
  width: 100%;
  min-height: 1rem;
  border: 1px dashed gray;
}
</style>
