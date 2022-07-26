<template>
  <main>
    <!-- Section 1 Hero -->
    <section><Hero /></section>

    <!-- Section 2 Claim -->
    <section id="claim" class="brand_primary">
      <div class="container">
        <div class="row">
          <div class="col-8 offset-2">
            <h2 class="text-white font_bold">
              <span class="text-uppercase">world class</span> Fitness
            </h2>
            <img
              class="mb-4 mt-4"
              src="../assets/img/divider-xx-red.png"
              alt="doubleX_divider"
            />
            <p>
              At Avada gym, everything we do from top to bottom is of the
              highest quality to ensure we're equipped to help you reach your
              goals of a healthy and fit lifesstyle.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Section 3 Form -->
    <section class="brand_secondary">
      <img src="../assets/img/home_img-compressor.jpg" alt="" />
    </section>

    <!-- Section 4 Offers -->
    <section id="offers"></section>

    <!-- Section 5 Reviews and Locations -->
    <section class="brand_primary">
      <section id="locations"></section>
    </section>

    <!-- Section 6 Quote -->
    <section id="quote"></section>

    <!-- Section 7 Trainers -->
    <section class="brand_secondary">
      <div class="container pt-5">
        <div class="row pt-5">
          <div class="col-8 offset-2">
            <h2 class="text-white font_bold text-uppercase">
              Meet our trainers
            </h2>
            <img
              class="mb-4 mt-4"
              src="../assets/img/divider-xx-red.png"
              alt="doubleX_divider"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- Section 8 News -->
    <section class="brand_primary"></section>
  </main>
</template>

<script>
import Hero from "./Hero.vue";

export default {
  name: "Main",
  components: {
    Hero,
  },
};
</script>



<style lang="scss" scoped>
@import "../style/variables.scss";

main {
  margin-top: -200px;
}

.font_bold {
  font-family: "Ubuntu", sans-serif;
}

// Common sections classes
.brand_primary {
  background-color: $brandPrimary;
  height: 40vh;
}

.brand_secondary {
  background-color: $brandSecondary;
  height: 40vh;
}

// Section 2 Claim
#claim {
  display: flex;
  align-items: center;
  justify-content: center;
}

p {
  color: $thintextcolor;
}

// Section 4 Offers
#offers {
  background-image: url("../assets/img/gym_bkgd_bw-compressor.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 60vh;
}

// Section 4 Offers
#quote {
  background-image: url("../assets/img/home-testimonial-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 60vh;
}
</style>