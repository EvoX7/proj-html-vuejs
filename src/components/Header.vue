<template>
  <header>
    <NavBar />
  </header>
</template>

<script>
import NavBar from "./NavBar.vue";

export default {
  name: "Header",
  components: {
    NavBar,
  },
};
</script>


 <style lang="scss" scoped>
header {
  background-color: #121315;
}
</style>