<template>
   <h1>Blog Post</h1>
   <button @click="toggleAddBlog" class="btn">Add Blog</button>

</template>

<script>
 export default{
    name: "HeaderSection" ,

methods: {
  toggleAddBlog(){
   this.$emit("toggle-add-blog")
  }
}
 }


</script>

<style>



</style>