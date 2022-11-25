<template>
  <div class="container-sm">
    <div class="row">
      <div class="">
        <SingleCardComp />
      </div>
    </div>
  </div>
</template>

<script>
import SingleCardComp from "./SingleCardComp.vue";
export default {
  name: "MainComp",
  components: {
    SingleCardComp,
  },
};
</script>

<style lang="scss" scoped></style>
