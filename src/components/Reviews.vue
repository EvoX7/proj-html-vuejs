<template>
  <div class="container ">
    <div class="card rounded-0 " style="width: 500px">
      <div class="row">
        <div class="col-4">
          <img class="p-3" :src="reviews.img" alt="reviews" />
        </div>
        <div class="col-8">
          <div class="card-body">
            <p class="card-text text-white-50 fw-lighter fst-italic">
              {{ reviews.text }}
            </p>
            <p class="card-text font_bold text-white-50">
              {{ reviews.signature }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Reviews",
  props: ["reviews"],
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.font_bold {
  font-family: "Ubuntu", sans-serif;
}

.card {
  text-align: left;
  background-color: $brandSecondary;
}
</style>