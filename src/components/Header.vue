<template>
  <nav>
    <input type="text" @input="getWeather($event.target.value)" />
    <button @click="toggleDarkMode">Alterar Tema</button>
  </nav>
</template>

<script>
export default {
  name: "Header",
  methods: {
    getWeather(value) {
      this.$emit("getWeather", value);
    },
    toggleDarkMode() {
      this.$emit("toggleDarkMode");
    },
  },
};
</script>
<style scoped lang="scss"></style>
