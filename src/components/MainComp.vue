<template>
  <div class="container-card">
    <div class="card text-center" style="width: 18rem">
      <img
        :src="card.poster"
        class="card-img-top p-3 text-white"
        alt="Immagine non disponibile"
      />
      <div class="card-body">
        <h5 class="card-title fs-4 text-white">{{ card.title }}</h5>

        <div class="text-secondary">
          {{ card.author }}
        </div>
        <div class="text-secondary">
          {{ card.year }}
        </div>
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
  background-color: #2d3a46;
}
</style>
