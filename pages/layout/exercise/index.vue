<template>
  <Container nogutter>
    <Row nogutter>
      <Column :xs="2" :sm="2" :md="2" class="block orange"/>
      <Column :xs="2" class="block green-small"/>
      <Column :xs="6" :sm="12" :md="10" class="block blue"/>
    </Row>
    <div class="mt-1"/>
    <Row nogutter>
      <Column :md="2" class="block green-big"/>
      <Column :xs="12" :sm="12" :md="10">
        <Row nogutter>
          <Column :xs="12" :sm="12" :md="4" class="block pink"/>
          <Column :xs="12" :sm="12" :md="8">
            <Row nogutter between>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
            </Row>
            <Row nogutter between>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
              <Column :xs="12" :sm="6" :md="3" class="block gray"/>
            </Row>
          </Column>
        </Row>
        <div class="mt-1"/>
        <Row nogutter between>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
          <Column :xs="12" :sm="6" :md="1" class="block gray"/>
        </Row>
      </Column>
    </Row>
  </Container>
</template>

<script>
export default {

}
</script>
<style lang="scss" scoped>
@import "assets/components/layout/layoutSystem.scss";
</style>
