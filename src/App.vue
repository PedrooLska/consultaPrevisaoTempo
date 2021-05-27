<template>
  <div :class="{ 'theme--dark': darkMode }">
    <Header
      @getWeather="(value) => getWeather(value)"
      @toggleDarkMode="toggleDarkMode"
    />
    <Card />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Card from "@/components/Card.vue";

export default {
  components: {
    Header,
    Card,
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
    getWeather(value) {
      console.log(value);
    },
  },
};
</script>

<style lang="scss">
body {
  display: flex;
  align-content: center;
  justify-content: center;
}

.theme--dark {
  background: black;
}
</style>
