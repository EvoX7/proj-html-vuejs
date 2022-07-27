<template>
  <div class="container d-flex">
    <div class="row">
      <div class="col-6 m-auto">
        <h2 class="text-white mb-5">{{ quotes.text }}
        </h2>
        <h5 class="text-white text-uppercase font_bold">{{ quotes.signature }}</h5>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name:"Quote",
    props: ["quotes"],
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

h2 {
    line-height: 50px;
}

.font_bold {
  font-family: "Ubuntu", sans-serif;
}
</style>