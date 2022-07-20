
<template>
<div>
    <!-- <h1 style="white-space:pre-line; color: aqua;">{{message}}</h1>
    <textarea type="text" v-model="message"/> -->
    <button v-on:click="updateTitle">Update Title</button>

</div>
</template>
<script>
export default{
    name:"first-file",
    methods:{
        updateTitle(){
            this.$emit('changeTitle',' changed...  props has been passed')
        }

    }
     
};
</script>
<!-- <style>
.vueStyle{
    color:orange
}
.display{
    background-color: beige;
    padding: 5px;
}
</style> -->
