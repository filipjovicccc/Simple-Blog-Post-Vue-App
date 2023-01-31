<template>
  <HeaderSection  @toggle-add-blog="toggleAddBlog"/>
  <div v-show="showAddBlog">
  <NewBlog @add-blog="addBlog"/>
  
  </div>
  <BlogData />
  <BlogList :blogs="blogs"/>
  
</template>

<script>
 import BlogData from "./components/BlogData.vue"
 import BlogList from "./components/BlogList.vue"
 import NewBlog from "./components/NewBlog.vue"
 import HeaderSection from "./components/HeaderSection.vue"

export default {

  name: 'App',
  components: {
   // eslint-disable-next-line   
   BlogData,
   BlogList,
   NewBlog,
   HeaderSection

  },
  data(){
    return{
        blogs: [],
        showAddBlog: false
    }
  },
  methods:{
    toggleAddBlog(){
        this.showAddBlog = !this.showAddBlog
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
