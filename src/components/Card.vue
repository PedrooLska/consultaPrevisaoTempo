<template>
  <div class="card">
    <img :src="{ urlImg }" alt="Image Not Found" />
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    urlImg: String,
  },
};
</script>
<style scoped lang="scss"></style>
