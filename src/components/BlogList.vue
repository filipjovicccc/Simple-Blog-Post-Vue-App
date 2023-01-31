<template>
  <div class="blog-list">
 
      <article class="article" v-for="blog in blogs" :key="blog.id">
        <img class="images" :src="blog.img" alt="Image">
        <div class="section">
            <h2>{{ blog.title }}</h2> 
        </div>
            <p>{{ blog.text }}</p> 
      </article>
   
  </div>
</template>
<script>
  export default {
    name: 'BlogList',
    props: ['blogs']
  }
</script>

<style>

 .article{

  width: 300px;
  margin: 20px;
  text-align: left;
}

.article h2{
  text-align: centar;

}

.images{
  width: 300px;
  height: 200px;
  border-radius: 9px 9px 9px 9px;
}


.section{
  display: flex;
 align-items: center;
 padding: 3px
}
.section h2{
  margin-right: 20px;
}
 .btn-section {
     display: flex;
    padding: 10px;
    justify-content: space-between;
    width: 200px;

 
}

.btn {
  background-color: rgb(0, 34, 255);
  width: 150px;
  height: 38px;
  border-radius: 7px 7px 7px 7px;
  color: white;
}


@media(max-width:778px){

}


@media(max-width:500px){
 .article{width: 185px;}
}

</style>