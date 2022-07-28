<template>
  <div class="container d-flex justify-content-between">
    <ul class="pt-5">
      <li class="d-flex" v-for="(links, index) in bottomFooter" :key="index">
        <p class="text-white-50 px-2">&copy;{{ links.rights }} |</p>
        <p class="text-white-50">
          <a href="#">{{ links.theme }}</a> |
        </p>
        <p class="text-white-50 px-2">{{ links.reserved }} |</p>
        <p class="text-white-50 px-2 ps-1">
          <a href="#">{{ links.creator }}</a>
        </p>
      </li>
    </ul>
    <div class="socials me-1 mt-4 text-white">
      <div class="icons_bg"><i class="fa-brands fa-facebook-f"></i></div>
      <div class="icons_bg ms-2"><i class="fa-brands fa-twitter"></i></div>
      <div class="icons_bg ms-2">
        <i class="fa-brands fa-instagram"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BottomFooter",

  data() {
    return {
      // Footer links
      bottomFooter: [
        {
          rights: "Copyright 2012 - 2022",
          theme: "Avada Theme by Theme Fusion",
          reserved: "All rights reserved",
          creator: "Powered by WordPress",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";

li {
  font-size: 0.9em;
  list-style: none;
  letter-spacing: 1px;
}

a {
  text-decoration: none;
  color: #8f9091;

  &:hover {
    color: $brandTertiary;
  }
}

i {
  display: flex;
  line-height: 45px;
  justify-content: center;
  font-size: 1.2em;

  &:hover {
    color: $brandPrimary;
    cursor: pointer;
  }
}

.socials {
  color: white;
  display: flex;
}

.icons_bg {
  border-radius: 5px;
  width: 45px;
  height: 45px;
  margin-bottom: 30px;
  background-color: $brandTertiary;
}
</style>