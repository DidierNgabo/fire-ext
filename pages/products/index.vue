<template>
  <div>
    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0, 1)"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="smallCard in smallCardInfo.slice(0, 1)"
        :key="smallCard.id"
        :card="smallCard"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    };
  }
};
</script>

<style></style>
