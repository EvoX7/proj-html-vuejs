<template>
  <div id="locations" class="container pt-5 pb-5">
    <div class="row">
      <div class="col-12">
        <img class="p-4" src="../../assets/img/home-image1.jpg" alt="" />
        <img class="p-4" src="../../assets/img/home-image2.jpg" alt="" />
        <img class="p-4" src="../../assets/img/home-image3.jpg" alt="" />
        <img class="p-4" src="../../assets/img/home-image4.jpg" alt="" />
        <img class="p-4" src="../../assets/img/home-image54.jpg" alt="" />
        <img class="p-4" src="../../assets/img/home-image6.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Locations",
  props: ["locations"],
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

#locations {
  display: flex;
  flex-wrap: wrap;
}

img {
  position: relative;
  display: inline-block;
  -webkit-transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
  transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
}

img:hover {
  transform: scale(1.1);
}
</style>