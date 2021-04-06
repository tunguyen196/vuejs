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