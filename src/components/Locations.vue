<template>
  
    <div class="container">
        <div class="row">
            <div class="col-1">
                <img :src="locations.img" alt="locations">
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