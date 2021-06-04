<template>
  <div>
    <h4>Number in the parent: {{number}}</h4>
    <Child :message="message" @increaseNumber="increaseNumber"/>
    <button @click="increaseNumber">Increase number in Parent</button>
  </div>
</template>

<script>
import Child from "./Child";

export default {
  data() {
    return {
      message: "Hello world",
      number: 1
    }
  },
  components: {
    Child
  },
  methods: {
    increaseNumber() {
      this.number ++
    }
  }
}
</script>
