<template>
  <div class="wrapper">
    <div class="container">
      <h2>Seller App</h2>
      <nuxt-link class="button" to="new-call">Appeler un vendeur</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style lang="scss" scoped>
div {
  h2 {
    color: black;
  }
}
</style>
