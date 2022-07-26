<template>
<div>
  <header>
    <NavBar />
  </header>
  </div>
</template>

<script>
import NavBar from "./NavBar.vue";
import Hero from "./Hero.vue";

export default {
  name: "Header",
  components: {
    NavBar,
    Hero,
  },
};
</script>


 <style lang="scss" scoped>
 
header {
    
    background-color: red;
    height: 150px;
 
}
</style>