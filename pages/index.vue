<template>
<div class="wrapper">
  <div class="container">
    <h2>Seller App</h2>
  </div>
</div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style lang="scss" scoped>
div {
  h2 {
    color: red;

    @include desktop {
      color: blue;
    }

  }
}
</style>