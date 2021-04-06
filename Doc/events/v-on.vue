<template>
  <div id="app">
 
    <input type="text" v-model="name" />
    <br>
    <button v-on:click="name= 'abc'"></button>
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

