<template>
  <footer>
    <!-- Section 1 Join Us  -->
    <section id="joinus">
      <div id="wrapperft1">
        <div>
          <h2 class="font_bold text-white">Achieve Your Fitness Goals</h2>
          <p class="text-white">
            Flexible membership packages to suit all levels of athlete and
            achieve your fitness goals
          </p>
        </div>
        <div><BtnOutlined /></div>
      </div>
    </section>

    <!-- Section 2 Info  -->
    <section class="brand_primary">
        <div>
            <div></div>
            <div></div>
        </div>
    </section>

    <!-- Section 3 Copyright/Socials  -->
    <section id="bottom" class="brand_secondary">
        <!-- <h5 class="text-uppercase">come find us</h5>
        <h5 class="text-uppercase">recent posts</h5>
        <h5 class="text-uppercase">opening times</h5> -->
    </section>
  </footer>
</template>

<script>
import Button from "./BtnFull.vue";
import BtnOutlined from "./BtnOutlined.vue";

export default {
  components: {
    Button,
    BtnOutlined,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

// Common sections classes
.brand_primary {
  background-color: $brandPrimary;
  height: 40vh;
}

.brand_secondary {
  background-color: $brandSecondary;
  height: 10vh;
}


.font_bold {
  font-family: "Ubuntu", sans-serif;
}

// Wrapper 1st sub-footer 
#wrapperft1 {
    height: 100%;
    display: flex;
    justify-content: space-evenly;
    align-items:center;
    text-align: left;
}

// Section 1 background
#joinus {
  height: 20vh;
  background-image: url(../assets/img/home-parallax.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position-y: 16%;
}


// Sezione 3 Bottom

</style>