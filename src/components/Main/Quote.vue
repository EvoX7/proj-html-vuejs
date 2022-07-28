<template>
  <div class="container d-flex">
    <div class="row">
      <div class="col-6 m-auto">
        <h2 class="text-white mb-5">{{ quotes.text }}</h2>
        <img
          class="pb-5 mb-5"
          src="../../assets/img/divider-white-xx.png"
          alt=""
        />
        <h5 class="text-white text-uppercase fw-bold pb-5">
          {{ quotes.signature }}
        </h5>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Quote",
  props: ["quotes"],
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

h2 {
  font-family: "Open Sans", sans-serif;
  line-height: 50px;
  text-shadow: 1px 1px #000000;
}

h5 {
  font-family: "Open Sans", sans-serif;
  text-shadow: 1px 1px #000000;
}

img {
  width: 30px;
  height: 60px;
}
</style>