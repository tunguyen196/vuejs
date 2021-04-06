<template>
  <div id="app">
    <Prop v-for="(task, index) in tasks" :key="index" :taskData="task"  />
    <Demo />
  </div>
</template>

<script>
import Prop from "./prop-component.vue"
import Demo from "./Demo.vue"
export default {
  name: "App",
  data() {
    return {
      newTask: "",
      tasks: [
        {content:'di choi'},
        {content:'code'},
      ],
    };
  },
  components: {
    Prop,
    Demo,
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
