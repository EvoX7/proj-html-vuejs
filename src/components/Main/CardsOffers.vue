<template>
  <div>
    <div class="container bg-transparent">
      <div id="circle">
        <img class="icons mb-4" :src="offers.img" alt="offers" />
      </div>
      <h5 class="font_bold text-white">{{ offers.title }}</h5>
      <img src="../../assets/img/divider-x-red.png" alt="gym-offers" />
      <p class="text-white-50 mt-2">{{ offers.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardsOffers",

  props: ["offers"],
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

.font_bold {
  font-family: "Ubuntu", sans-serif;
}

.icons {
  display: inline;
  margin: 0 auto;
  height: 50px;
  width: auto;
  position: relative;
  top: 25px;

}

#circle {
  margin:0 auto;
  width: 100px;
  height: 100px;
  overflow: hidden;
  border-radius: 50%;
  border: 1px solid $brandTertiary;
  margin-bottom: 20px;
  
}

</style>