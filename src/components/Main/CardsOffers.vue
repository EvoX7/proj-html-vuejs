<template>
  <div>
    <div class="container bg-transparent">
      <img class="icons mb-4" :src="offers.img" alt="offers" />
      <h5 class="font_bold text-white">{{ offers.title }}</h5>
      <img src="../../assets/img/divider-x-red.png" alt="gym-offers" />
      <p class="text-white-50 mt-2">{{ offers.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardsOffers",

  props: ["offers"]


};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

.font_bold {
  font-family: "Ubuntu", sans-serif;
}

.icons {
  border: 2px solid $brandTertiary;
  border-radius: 50%;
  padding:10px;
  width: 90px;
  height: 90px;
}
</style>