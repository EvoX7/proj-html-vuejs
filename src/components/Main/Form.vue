<template>
  <div id="form" class="container">
    <div class="row">
      <div class="col-6">
        <img
          class="img-fluid"
          src="../../assets/img/home_img-compressor.jpg"
          alt="home_img-compressor"
        />
      </div>

      <div class="col-5">
        <h4 class="text-white font_bold">Sign Up for a free training session!</h4>
        <form>
          <div class="mb-3 mt-4">
            <label for="exampleNameInput" class="form-label text-white-50">Name*</label>
            <input
              type="text"
              class="form-control rounded-0 bg-dark border border-secondary text-white"
              id="exampleNameText"
            />

            <div class="mb-4 mt-4 text-left">
              <label for="exampleInputEmail1" class="form-label text-white-50"
                >Email</label
              >
              <input
                type="email"
                class="form-control rounded-0 bg-dark border border-secondary text-white"
                id="exampleInputEmail1"
              />
            </div>
            <BtnFull />
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>

import BtnFull from "./BtnFull.vue";
export default {
  name: "Form",
  components: {
    BtnFull,
  },
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";
.font_bold {
  font-family: "Ubuntu", sans-serif;
}


</style>