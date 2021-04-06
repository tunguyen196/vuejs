<template>
  <div id="app">
 
    <h1 type="text" v-bind:tudz="name" :ggg="name2" :class="{test:selected}"></h1>
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
      name2: 'ssss',
      selected:true
    };
  },
  
};
</script>

