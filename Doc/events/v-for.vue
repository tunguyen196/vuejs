<template>
  <div id="app">
    <input type="text" v-model="addTask">
    <button @click="tasks.push({todo:addTask,done:true})">them</button>
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
      tasks: [
        { todo: 'di cho', done:false},
        { todo: 'nau an', done:false},
        { todo: 'code', done:false},
        { todo: 'di vs', done:false},
      ]
    };
  },
};
</script>
