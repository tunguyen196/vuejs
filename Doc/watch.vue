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
  },
  watch: {
    newTask: function(newValue, oldValue){
      alert(newValue+'--'+oldValue);
    }
  }
};
</script>