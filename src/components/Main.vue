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
    <section id="form_section" class="brand_secondary">
      <Form />
    </section>

    <!-- Section 4 Offers -->
    <section id="offers">
      <CardsOffers class="col-2 mb-3" v-for="(offer, index) in offers" :key="index" :offers="offer"/>
    </section>

    <!-- Section 5 Reviews and Locations -->
    <section class="brand_primary reviews pt-5">
      <div class="container">
        <div class="row">
          <div class="col-10 m-auto">
            <h2 class="text-white font_bold text-uppercase">
              Real world results
            </h2>
            <img
              class="mb-4 mt-4"
              src="../assets/img/divider-xx-red.png"
              alt="doubleX_divider"
            />
          </div>
          <Reviews class="col-6 mb-3" v-for="(review, index) in reviews" :key="index" :reviews="review" />
        </div>
      </div>

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

<!-- sinistra -->

<!-- 1 -->
        <div>

        </div>

<!-- 2  -->
        <div>

        </div>
<!-- destra  -->
        <div></div>
        <div></div>
      </div>
    </section>

    <!-- Section 8 News -->
    <section class="brand_primary"></section>
  </main>
</template>

<script>
import Hero from "./Hero.vue";
import Form from "./Form.vue";
import CardsOffers from "./CardsOffers.vue";
import Reviews from "./Reviews.vue";

export default {
  name: "Main",
  components: {
    Hero,
    Form,
    CardsOffers,
    Reviews,
  },
  data() {
    return {

      // Gym Offers
      offers: [
        {
          title: "Strenght & Conditioning",
          img: require("../assets/img/Link.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
        {
          title: "Fitness & Cardio",
          img: require("../assets/img/Bycicle.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
        {
          title: "Flexibility & rest",
          img: require("../assets/img/CloudFlex.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
        {
          title: "Health & Diet",
          img: require("../assets/img/HearthIcon.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
      ],


      // Reviews
      reviews: [
        {
          img: require("../assets/img/review_1-compressor.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Tara Smith"
        },
        {
          img: require("../assets/img/review_3-compressor-2.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Simon Chel"
        },
        {
          img: require("../assets/img/review_2-compressor.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Jen Wirth"
        },
        {
          img: require("../assets/img/review_4-compressor-2.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Jeff Glum"
        },
      ]
    };
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
  
}

.brand_secondary {
  background-color: $brandSecondary;
}

// Section 2 Claim
#claim {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50vh;
}

p {
  color: $thintextcolor;
}

// Section 3 Form
#form_section {
  padding: 15rem;
  display: flex;
  align-items: center;
  // height: 50vh;
}

// Section 4 Offers
#offers {
  display: flex;
  justify-content: center;
  align-items: center;
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