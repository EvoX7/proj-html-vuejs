<template>
  <div>
    <div class="card rounded-0">
      <img :src="trainers.img" alt="trainers" />
      <div class="card-body ms-4">
        <h6 class="card-title text-white font_bold mt-3">
          {{ trainers.name }}
        </h6>
        <h6 class="card-title text-white font_bold mb-4">{{ trainers.job }}</h6>
        <p class="card-text text-white-50">
          {{ trainers.text }}
        </p>
        <div class="socials mt-4">
          <div class="icons_bg"><i class="fa-brands fa-facebook-f"></i></div>
          <div class="icons_bg ms-2"><i class="fa-brands fa-twitter"></i></div>
          <div class="icons_bg ms-2">
            <i class="fa-brands fa-instagram"></i>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>

import BtnOutlined from "./BtnOutlined.vue";
export default {
  name: "TrainersCards",
  props: ["trainers"],
  components: {
    BtnOutlined,
  }
};
</script>

<style lang="scss" scoped>
@import "../../style/variables.scss";
.font_bold {
  font-family: "Ubuntu", sans-serif;
}

.card {
  width: 23rem;
  text-align: left;
  background-color: $brandPrimary;
}

p {
  line-height: 30px;
}

.socials {
  color: white;
  display: flex;
}

i {
  display: flex;
  line-height: 45px;
  justify-content: center;
  font-size: 1.2em;

  &:hover {
    color: $brandTertiary;
    cursor: pointer;
  }
}

.icons_bg {
  border-radius: 5px;
  width: 45px;
  height: 45px;
  margin-bottom:30px;
  background-color: $brandSecondary;
}

img {
position: relative;
  display: inline-block;
  -webkit-transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
  transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
}

img:hover{
    transform: scale(1.1);
    border-radius: 5px;
  box-shadow: 0 10px 5px rgba(0, 0, 0, 0.3);
}


</style>