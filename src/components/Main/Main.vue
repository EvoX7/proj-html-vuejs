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
              src="../../assets/img/divider-xx-red.png"
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
      <CardsOffers
        class="col-2 mb-3"
        v-for="(offer, index) in offers"
        :key="index"
        :offers="offer"
      />
    </section>

    <!-- Section 5 Reviews and Locations -->

    <!-- Reviews -->
    <section class="brand_primary reviews pt-5">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <h2 class="text-white font_bold text-uppercase mt-5">
              Real world results
            </h2>
            <img
              class="mb-5 mt-4"
              src="../../assets/img/divider-xx-red.png"
              alt="doubleX_divider"
            />
          </div>
          <Reviews
            class="col-6 mb-3"
            v-for="(review, index) in reviews"
            :key="index"
            :reviews="review"
          />
        </div>
      </div>
      <!-- Locations  -->
      <div class="container pt-5 mt-5">
        <div class="row">
          <div class="col-12">
            <h2 class="text-white font_bold text-uppercase">
              High performance facilities
            </h2>
            <img
              class="mb-4 mt-4"
              src="../../assets/img/divider-xx-red.png"
              alt="doubleX_divider"
            />
          </div>
        </div>
      </div>
      <section>
        <Locations />
      </section>
    </section>

    <!-- Section 6 Quote -->
    <section id="quote">
      <Quote v-for="(quote, index) in quotes" :key="index" :quotes="quote" />
    </section>

    <!-- Section 7 Trainers -->
    <section id="trainers" class="brand_secondary p-5">
      <div class="container pt-5">
        <div class="row me-5 pt-5">
          <div class="col-12 ms-5">
            <h2 class="text-white font_bold text-uppercase">
              Meet our trainers
            </h2>
            <img
              class="mb-5 mt-4"
              src="../../assets/img/divider-xx-red.png"
              alt="doubleX_divider"
            />
          </div>
          <TrainersCards
            class="col-3 m-auto mb-5"
            v-for="(trainer, index) in trainers"
            :key="index"
            :trainers="trainer"
          />
        </div>
      </div>
      <BtnOutlined value="view all trainers" />
    </section>

    <!-- Section 8 News -->
    <section class="brand_primary">
      <div class="container pt-5">
        <div class="row me-5 pt-5">
          <div class="col-12 ms-5">
            <h2 class="text-white font_bold text-uppercase">
              Performance news
            </h2>
            <img
              class="mb-5 mt-4"
              src="../../assets/img/divider-xx-red.png"
              alt="doubleX_divider"
            />
          </div>
        </div>
      </div>
      <PerformanceCards
        v-for="(perform, index) in performance"
        :key="index"
        :performance="perform"
      />
    </section>
  </main>
</template>

<script>
import Hero from "./Hero.vue";
import Form from "./Form.vue";
import CardsOffers from "./CardsOffers.vue";
import Reviews from "./Reviews.vue";
import Locations from "./Locations.vue";
import Quote from "./Quote.vue";
import TrainersCards from "./TrainersCards.vue";
import PerformanceCards from "./PerformanceCards.vue";
import BtnOutlined from "./BtnOutlined.vue";

export default {
  name: "Main",
  components: {
    Hero,
    Form,
    CardsOffers,
    Reviews,
    Locations,
    Quote,
    TrainersCards,
    PerformanceCards,
    BtnOutlined,
  },
  data() {
    return {
      // Gym Offers
      offers: [
        {
          title: "Strenght & Conditioning",
          img: require("../../assets/img/Link.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
        {
          title: "Fitness & Cardio",
          img: require("../../assets/img/Bycicle.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
        {
          title: "Flexibility & rest",
          img: require("../../assets/img/CloudFlex.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
        {
          title: "Health & Diet",
          img: require("../../assets/img/HearthIcon.png"),
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque.",
        },
      ],

      // Reviews
      reviews: [
        {
          img: require("../../assets/img/review_1-compressor.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Tara Smith",
        },
        {
          img: require("../../assets/img/review_3-compressor-2.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Simon Chel",
        },
        {
          img: require("../../assets/img/review_2-compressor.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Jen Wirth",
        },
        {
          img: require("../../assets/img/review_4-compressor-2.jpg"),
          text: '"Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, quibusdam atque."',
          signature: "- Jeff Glum",
        },
      ],

      // Quotes
      quotes: [
        {
          text: '"I fear not the man who has practiced 10,000 kicks once, but i fear the man who has practiced one kick 10,000 times"',
          signature: "Bruce Lee - Quote of the day",
        },
      ],

      // Trainers cards
      trainers: [
        {
          img: require("../../assets/img/trainer1-400x297.jpg"),
          name: "Ann baker",
          job: "Personal Trainer",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quae minima et laudantium vitae id.",
        },
        {
          img: require("../../assets/img/trainer3-400x297.jpg"),
          name: "Anne warren",
          job: "Personal Trainer",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quae minima et laudantium vitae id.",
        },
        {
          img: require("../../assets/img/trainer4-400x297.jpg"),
          name: "Peter Rice",
          job: "Personal Trainer",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quae minima et laudantium vitae id.",
        },
      ],

      // Performance cards
      performance: [
        {
          img: require("../../assets/img/blog1-400x208.jpg"),
          title: "Train with free weights or your body weight?",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam deleniti natus ratione sequi culpa omnis porro delectus quae, quasam dolores autem molestias vero? Ex.Veniam deleniti natus ratione[...]",
        },
        {
          img: require("../../assets/img/blog4-400x289.jpg"),
          title: "Nutritional advice that will keep you training",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam deleniti natus ratione sequi culpa omnis porro delectus quae, quasam dolores autem molestias vero? Ex.Veniam deleniti natus ratione[...]",
        },
        {
          img: require("../../assets/img/blog6-400x400.jpg"),
          title: "Simple principles for your next workout",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam deleniti natus ratione sequi culpa omnis porro delectus quae, quasam dolores autem molestias vero? Ex.Veniam deleniti natus ratione[...]",
        },
        {
          img: require("../../assets/img/trainer3-400x297.jpg"),
          title: "To be number one, train like you're number two",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam deleniti natus ratione sequi culpa omnis porro delectus quae, quasam dolores autem molestias vero? Ex.Veniam deleniti natus ratione[...]",
        },
        {
          img: require("../../assets/img/trainer4-400x297.jpg"),
          title: "Top 5 mistakes every gym member make",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam deleniti natus ratione sequi culpa omnis porro delectus quae, quasam dolores autem molestias vero? Ex.Veniam deleniti natus ratione[...]",
        },
        {
          img: require("../../assets/img/trainer1-400x297.jpg"),
          title: "The myths of shedding body fat explored",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam deleniti natus ratione sequi culpa omnis porro delectus quae, quasam dolores autem molestias vero? Ex.Veniam deleniti natus ratione[...]",
        },
      ],
    };
  },
};
</script>



<style lang="scss" scoped>
@import "../../style/variables.scss";

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
  height: 50vh;
}

// Section 4 Offers
#offers {
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url("../../assets/img/gym_bkgd_bw-compressor.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 60vh;
}
// Section 5 Locations

// Section 4 Offers
#quote {
  display: flex;
  background-image: url("../../assets/img/home-testimonial-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 60vh;
}
</style>