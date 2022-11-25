<template>
  <div class="container-card">
    <div class="card" style="width: 18rem">
      <img :src="card.poster" class="card-img-top" alt="" />
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">
          Some quick example text to build on the card title and make up the
          bulk of the card's content.
        </p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainComp",
  components: {},
  props: {
    card: Object,
  },
};
</script>

<style lang="scss" scoped>
.container-card {
  width: calc(100% / 5);
  padding: 20px;
}
.card {
}
</style>
