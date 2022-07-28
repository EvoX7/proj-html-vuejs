<template>
  <div>
    <button
      type="button" @click="submit"
      class="btn btn-lg btn-outline-light border-0 text-uppercase rounded-0 mt-3 px-5">start now!
    </button>
  </div>
</template>

<script>
export default {
  name: "BtnFull",
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

button {
  width: 100%;
  color: white;
  background-color: #ee6059;
  font-size: 1em;
}
</style>