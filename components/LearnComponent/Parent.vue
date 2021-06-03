<template>
  <div>
    <Child :message="message"/>
  </div>
</template>

<script>
import Child from "./Child";

export default {
  data() {
    return {
      message: "Hello world"
    }
  },
  components: {
    Child
  }
}
</script>
