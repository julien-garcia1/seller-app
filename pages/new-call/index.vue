<template>
  <div class="wrapper">
    <div class="container">
      <h2>Call a vendor here</h2>
      <form action="">
        <div class="input-section">
          <label for="name">Enter your name</label>
          <input type="text" name="name" id="name" v-model="name" />
        </div>
        <div class="input-section">
          <label for="section">Enter your section</label>
          <input type="text" name="section" id="section" v-model="section" />
        </div>
        <div class="submit">
          <div @click="callSeller" class="button">Call a seller !</div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: null,
      section: null,
    };
  },

  methods: {
    callSeller() {
      const url =
        "https://seller-app-83dbd-default-rtdb.firebaseio.com/clients.json";

      fetch(url, {
        method: "POST",
        body: JSON.stringify({
          id: 1,
          name: this.name,
          section: this.section,
        }),
      });
    },
  },
};
</script>
