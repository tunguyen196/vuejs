<template>
  <div id="app">
    <input type="text" v-model="newTask">
    <button @click="addTask()">them</button>
   <div v-for="(task, index) in tasks" :key="index">
     <input type="checkbox" v-model="task.done"> 
     <span :class="{done: task.done}">{{task.todo}}</span>
   </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      newTask:'',
      tasks: []
    };
  },
  methods:{
    addTask: function(){
      this.tasks.push({todo:this.newTask,done:false});
      this.newTask = '';
    }
  }
};
</script>

<style>
.done{
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
