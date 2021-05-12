<template>
  <div class="container">
    <h3 class="header">
      {{ card.title }}
    </h3>
    <div class="card-container">
      <SmallCard
        v-for="cardImg in card.cards"
        :key="cardImg.id"
        :card="cardImg"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ["card"]
};
</script>

<style scoped>
.container {
  padding: 2rem 0;
}

.header {
  font-weight: 700;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}

.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
