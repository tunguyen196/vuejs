<template>
  <div id="app">
    {{ total | addComma}}
    <button @click="total += 50000">Add 50k</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      total: 1000000,
    };
  },
  filters: {
    addComma: function(total) {
        return total.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    },
  },
};
</script>

<style>
.done {
  text-decoration: line-through;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size: 30px;
}
</style>
