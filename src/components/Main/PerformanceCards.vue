<template>
  <div class="container">
    <div class="row">
      <div class="col-1">
        <div class="card rounded-0">
          <img :src="performance.img" alt="trainers" />
          <div class="card-body ms-4">
            <h6 class="card-title text-white font_bold">
              {{ performance.title }}
            </h6>
            <p class="card-text text-white-50">{{ performance.text }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PerformanceCards",
  props: ["performance"],
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

.font_bold {
  font-family: "Ubuntu", sans-serif;
}

.container {
  display: flex;
  flex-flow: column;
}

.card {
  width: 20rem;
  margin-bottom: 50px;
  text-align: left;
  background-color: $brandSecondary;
}

img {
  &:hover {
    background-image: linear-gradient(
      to bottom,
      rgba(255, 0, 0, 0),
      rgba(255, 0, 0, 1)
    );
  }
}

h6 {
  font-size: 1.3em;
}

p {
  line-height: 25px;
  font-size: 0.8em;
}
</style>