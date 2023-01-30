<template>
  <form @submit="onSubmit">
  <label>Enter title name</label>
  <input type="text" v-model="title" name="title"/>
  <label>Enter blog text here</label>
  <input type="text" v-model="text" name="text" />
  <label>Enter img url</label>
  <input type="url" v-model="img" name="imgUrl"/>
  <div class="btn-section">
    <button type="submit" class="btn">Submit</button>
    <button class="btn">
    Close
    </button>
  </div>
  </form>

</template>

<script>

export default{
    name: "NeWBlog",
    
    data(){
        return{
            title: "",
            text: "",
            img: ""
        }
    },

    methods: {
        onSubmit(e){
            e.preventDefault()

             if(!this.title){
                alert("Please add a valid title")
                return
             }

              if(!this.text){
                alert("Please add a valid text")
                return
            }
            
              if(!this.img){
                alert("Please add a valid img")
                return
            }

            const newBlog = {
                id: Math.floor(Math.random() *1000),
                title: this.title,
                text: this.title,
                img: this.img
            }
            this.$emit("add-blog", newBlog)
            this.title= ""
            this.day = ""
            this.img= " "
  


        }
    }
}


</script>

<style>


</style>