
<template>
  <div id="app">
    <div v-if="isShow">
      <input type="text" v-model="name" />
    </div>
    <br />
    <button @click="isShow = !isShow">
      An/Hien
    </button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      isShow: true,
     };
  },
};
</script>
