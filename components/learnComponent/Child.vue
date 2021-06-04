<template>
  <div>
    {{message}}
      <button v-on:click="increaseNumber">Increase number</button>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  props: {
    message: {
      type: String,
      default: undefined
    },
    increaseNumber: {
      type: Function,
    }
  }
}
</script>
