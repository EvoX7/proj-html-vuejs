<template>
  <div>
    <button
      type="button"
      class="btn btn-outline-light btn-lg text-uppercase rounded-0 mt-3 fs-6">{{ value }} </button>
  </div>
</template>

<script>
export default {
  name: "BtnOutlined",
  props: {
    value: String,
  }
};
</script>

<style lang="scss" scoped>


button {
    color: rgb(188, 188, 188);
}
</style>