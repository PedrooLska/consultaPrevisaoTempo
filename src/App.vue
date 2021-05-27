<template>
  <body :class="{ 'theme--dark': darkMode }">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>

    <button @click="toggleDarkMode">CHEGUEI AQUII</button>
    <router-view />
  </body>
</template>

<script>
export default {
  data() {
    return {
      nightMode: false,
    };
  },
  computed: {
    darkMode() {
      return this.$store.state.darkMode;
    },
  },
  methods: {
    toggleDarkMode() {
      this.$store.commit({ type: "toggleDarkMode" });
    },
  },
};
</script>

<style lang="scss">
.theme--dark {
  background: black;
}
</style>
