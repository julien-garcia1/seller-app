<template>
  <div class="wrapper">
    <div class="container">
      <h2>Welcome on admin page</h2>
      <div class="calls">
        <div class="call" v-for="client in clients" :key="client.id">
          <h3>{{ client.name }}</h3>
          <p>{{ client.section }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      clients: null,
    };
  },
  mounted() {
    const url =
      "https://seller-app-83dbd-default-rtdb.firebaseio.com/clients.json";

    fetch(url, {
      method: "GET",
    })
      .then((response) => response.json())
      .then((data) => (this.clients = data));
  },
};
</script>
