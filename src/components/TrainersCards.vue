<template>
  <div>
    <div class="card rounded-0 ">
      <img :src="trainers.img"  alt="trainers" />
      <div class="card-body ms-4">
        <h6 class="card-title text-white font_bold mt-3">{{trainers.name}}</h6>
        <h6 class="card-title text-white font_bold mb-4">{{trainers.job}}</h6>

        <p class="card-text text-white-50">
         {{trainers.text}}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TrainersCards",
  props: ["trainers"],
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.font_bold {
  font-family: "Ubuntu", sans-serif;
}

.card {
    width: 23rem;
    text-align: left;
    background-color: $brandPrimary;
}

p {
    line-height: 30px;
}
</style>