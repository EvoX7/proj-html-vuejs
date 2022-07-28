<template>
  <div>
    <div id="hero">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <h1 class="text-white font_bold">NO PAIN NO GAIN</h1>
            <p class="mt-3">
              Motivation is what gets you started. Habit is what keeps you
              going.
            </p>
            <BtnOutlined value="join us today"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BtnOutlined from "./BtnOutlined.vue";


export default {
  name: "Hero",

  components: {
    BtnOutlined,
  },
};
</script>

<style lang="scss" scoped>
.font_bold {
  font-family: "Ubuntu", sans-serif;
}

#hero {
  display: flex;
  justify-content: center;
  align-items: center;
  background: url("../../assets/img/home-banner.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
}

h1 {
  margin-top: 120px;
  font-size: 6.5em;
}

p {
  color: #c2c2c2;
  font-size: 1.2em;
}
</style>