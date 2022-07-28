<template>
  <div id="wrapper-links">
    <div class="container d-flex justify-content-around">
      <nav id="footer-nav">
        <!-- Come find us -->
        <ul>
          <h6 class="text-uppercase text-secondary mb-5">come find us</h6>
          <li v-for="(info, index) in findUs" :key="index">
            <p class="text-white-50">{{ info.address }}</p>
            <p class="text-white-50">{{ info.city }}</p>
            <p class="text-white-50">{{ info.phone }}</p>
            <p class="text-white-50">
              Email: <a href="#">{{ info.email }}</a>
            </p>
          </li>
        </ul>

        <!-- Recent posts -->
        <ul class="w-25 ms-5 me-5">
          <h6 class="text-uppercase text-secondary mb-5">recent posts</h6>
          <li v-for="(post, index) in recentPosts" :key="index">
            <p class="text-white-50">{{ post.train }}</p>
            <hr class="text-secondary" />
            <p class="text-white-50">{{ post.nutrition }}</p>
            <hr class="text-secondary" />
          </li>
        </ul>

        <div id="central-column-footer">
          <!-- Opening times  -->
          <ul class="me-4">
            <h6 class="text-uppercase text-secondary mb-5">opening times</h6>
            <li v-for="(week, index) in opening" :key="index">
              <p class="text-white-50">{{ week.week1 }}</p>
              <p class="text-muted">{{ week.hour1 }}</p>
              <p class="text-white-50">{{ week.week2 }}</p>
              <p class="text-muted">{{ week.hour2 }}</p>
            </li>
          </ul>
        </div>
        <div class="ms-3">
          <img id="ad" src="../../assets/img/gym_ad-compressor.jpg" alt="ad" />
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterLinks",

  data() {
    return {
      // Footer links
      findUs: [
        {
          address: "12345 North Main Street",
          city: "New York, NY 55555",
          phone: "Phone: 1.800.555.6789",
          email: "info@fitness-domain.com",
        },
      ],
      recentPosts: [
        {
          train: "Train with free weights or your body weight?",
          nutrition: "Nutrional advice that will keep you training",
        },
      ],
      opening: [
        {
          week1: "Weekdays Monday - Friday",
          hour1: "9:00 - 19:00",
          week2: "Weekends Saturday - Sunday",
          hour2: "9:00 - 21:00",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

li {
  list-style: none;
  letter-spacing: 1px;
}

a {
  text-decoration: none;
  color: rgb(160, 160, 160);

  &:hover {
    color: $brandTertiary;
  }
}

#footer-nav {
  text-align: left;
  margin-top: 70px;
  display: flex;
}
</style>