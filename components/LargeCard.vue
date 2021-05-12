<template>
  <nuxt-link :to="`/products/${card.id}`" class="card">
    <img :src="card.image" class="image" alt="fe" />
    <h3 class="header">
      {{ card.title }}
    </h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </nuxt-link>
</template>

<script>
export default {
  props: ["card"]
};
</script>

<style scoped>
a {
  text-decoration: none;
}
.card {
  width: 31.5%;
  height: 20rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  width: 90%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
  color: #000;
}
.header:hover {
  color: #000;
  text-decoration: none;
}
.snippet {
  color: grey;
}
</style>
