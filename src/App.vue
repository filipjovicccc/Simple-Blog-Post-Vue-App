<template>
  <BlogData />
  <BlogList />
  <NewBlog @add-blog="addBlog"/>
</template>

<script>
 import BlogData from "./components/BlogData.vue"
 import BlogList from "./components/BlogList.vue"
 import NewBlog from "./components/NewBlog.vue"

export default {

  name: 'App',
  components: {
   // eslint-disable-next-line   
   BlogData,
   BlogList,
   NewBlog

  },
  data(){
    return{
        blogs: [],
        showAddBlog: false
    }
  },
  methods:{
    toggleAddBlog(){
        this.showAddBlog = !this.sohwAddBlog
    },
    addBlog(blog){
        this.blogs =[...this.blogs, blog]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
