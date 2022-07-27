<template>
  <div>
    <div class="container ">
        <div class="row">
            <div class="col-12">
                <img :src="locations.img" alt="">
            </div>
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
@import "../style/variables.scss";
</style>