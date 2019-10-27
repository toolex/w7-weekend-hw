<template lang="html">
  <div class="">
      <h1>Studio Ghbli Films Info</h1>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      filmName: "",
      filmArray: []
    }
  },
  mounted() {
    fetch("https://ghibliapi.herokuapp.com/films")
    .then(response => response.json())
    .then(filmArrayData => this.filmArray = filmArrayData)


  }
};
</script>

<style lang="css" scoped>
</style>
