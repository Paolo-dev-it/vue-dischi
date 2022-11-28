<template>
  <div id="app">
    <HeaderComp />
    <div class="container">
      <select name="" id="">
        <option
          :value="element"
          v-for="(element, index) in dataSelect"
          :key="index"
        >
          {{ element }}
        </option>
      </select>
    </div>
    <div class="container-main">
      <div class="container-card">
        <MainComp
          v-for="(elem, index) in dataSongs"
          :key="index"
          :card="elem"
        />
      </div>
    </div>
  </div>
</template>

<script>
import HeaderComp from "./components/HeaderComp.vue";
import MainComp from "./components/MainComp.vue";

import axios from "axios";
export default {
  name: "App",
  components: {
    HeaderComp,
    MainComp,
  },
  data() {
    return {
      dataSongs: [],
      dataSelect: [],
    };
  },
  mounted() {
    this.getSongs();
  },
  methods: {
    getSongs() {
      axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((response) => {
          this.dataSongs = response.data.response;
          console.log(this.dataSongs);

          this.dataSongs.forEach((genreSingle) => {
            if (!this.dataSelect.includes(genreSingle.genre)) {
              this.dataSelect.push(genreSingle.genre);
            }
          });
        });
    },
  },
};
</script>

<style lang="scss">
.container-main {
  display: flex;
  justify-content: center;
}
.container-card {
  display: flex;
  flex-wrap: wrap;
  width: 80%;
}
#app {
  background-color: #1e2d3b;
}
</style>
