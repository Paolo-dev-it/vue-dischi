<template>
  <div id="app">
    <HeaderComp />
    <MainComp v-for="(elem, index) in dataSongs" :key="index" :card="elem" />
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
      dataSongs: "",
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
        });
    },
  },
};
</script>

<style lang="scss"></style>
