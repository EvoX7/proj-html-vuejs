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
        <div> <BtnOutlined value="join us"/></div>
      </div>
    </section>

    <!-- Section 2 Info  -->
    <section class="brand_primary">
      <FooterLinks />
    </section>

    <!-- Section 3 Copyright/Socials  -->
    <section id="bottom" class="brand_secondary">
      <BottomFooter />
    </section>
  </footer>
</template>

<script>

import BtnOutlined from "../Main/BtnOutlined.vue";
import FooterLinks from "./FooterLinks.vue";
import BottomFooter from "./BottomFooter.vue";

export default {
  components: {
    BtnOutlined,
    FooterLinks,
    BottomFooter,
  },
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

// Common sections classes
.brand_primary {
  background-color: $brandPrimary;
}

.brand_secondary {
  background-color: $brandSecondary;
}

.font_bold {
  font-family: "Ubuntu", sans-serif;
}

#wrapperft1 {
  height: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  text-align: left;
}

// Section 1 background
#joinus {
  height: 25vh;
  background-image: url(../../assets/img/home-parallax.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position-y: 16%;
}

// Sezione 3 Bottom
</style>