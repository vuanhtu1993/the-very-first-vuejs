<template>
  <div>
    <Header/>
    {{$route.params.id}}
  </div>
</template>

<script>
import Header from "../../../components/common/Header";
export default {
  components: {Header}
}
</script>
