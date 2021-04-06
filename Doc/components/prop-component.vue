<template>
    <div class="hello">
        <h1>{{taskData.content}}</h1>
    </div>
</template>
<script>
export default {
   props: ['taskData']
    // props: {
    //   taskData: {
    //     type:Object,
    //     default: function(){}
    //   }
    // }
}
</script>
<style scoped>

</style>
