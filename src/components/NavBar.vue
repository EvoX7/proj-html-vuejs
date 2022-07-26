<template>
  <div>
    <nav class="d-flex align-items-center justify-content-between ms-5">
      <div>
        <a href="."
          ><img class="ms-5" id="logo" src="../assets/img/gym_logo_1x.png" alt="gym_logo"
        /></a>
      </div>
      <ul class="d-flex me-5 pe-5">
        <li v-for="(link, index) in navBar" :key="index">
          <a :href="link.url">{{ link.text }}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      navBar: [
        {
          text: "home",
          url: "/#",
        },
        {
          text: "about us",
          url: "/#",
        },
        {
          text: "membership",
          url: "/#",
        },
        {
          text: "Testimonials",
          url: "/#",
        },
        {
          text: "blog",
          url: "/#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

nav {
    padding-top: 50px;
}

  li {
    text-transform: uppercase;
    font-size: 1em;
    list-style: none;
    margin: 0px 20px;
    transition: 0.3s;
  }

a {
    text-decoration: none;
    color: white;

    &:hover {
      color: $brandTertiary;
    }
}
</style>