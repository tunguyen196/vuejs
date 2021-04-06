<template>
  <div id="app">
 
    <input type="text" v-model="name" />
    <br>
    {{ name }}
  </div>
</template>

<script>


export default {
  name: "App",
  data() {
    return {
      name: "anh tu",
    };
  },
  
};
</script>

