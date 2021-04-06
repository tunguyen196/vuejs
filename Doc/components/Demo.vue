<template>
  <div class="display">
    <div
     v-for="(option, index) in options" :key="index"
     :class="{selected: option.done}"
     @click="option.done = !option.done"
     >
     <span>{{ option.name }}</span>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      options: [
        { name: "html", done: false },
        { name: "css", done: false },
        { name: "python", done: false },
        { name: "php", done: false },
        { name: "javascript", done: false },
        { name: "vuejs", done: false },
      ],
    };
  },
};
</script>
<style scoped>
.display div {
  display: inline-block;
  border: 1px solid #ebebeb;
  padding: 5px;
  margin: 5px;
  border-radius:5px;
  cursor: pointer;

}
.display div.selected{
    background: green;
    color: #fff;
   
}
</style>
