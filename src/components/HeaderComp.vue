<template>
  <div class="container-100">
    <div class="header">
      <img src="../assets/logo-small.svg" alt="" />
    </div>
    <!-- <div>
      <select name="" id="" v-model="userSelection">
        <option
          :value="element"
          v-for="(element, index) in dataSelect"
          :key="index"
          @keyup="$emit('nomeEmit', userSelection)"
        >
          {{ element }}
        </option>
      </select>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "HeaderComp",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  width: 100%;
  background-color: #2d3a46;
  padding: 10px;
  height: 10vh;
}
img {
  width: 50px;
}
</style>
