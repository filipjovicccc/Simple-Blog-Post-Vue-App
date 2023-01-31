
<template>
    <div >
    
      <BlogList :blogs="blogs"/>
    
    </div>

</template>

<script>
  import BlogList from './BlogList.vue'
 import image1 from "../assets/image1.avif"
 import image2 from "../assets/image2.avif"
 import image3 from "../assets/image3.avif"
 import image4 from "../assets/image4.avif"
 
  export default {
     name: 'BlogData',
     components: {
        BlogList
     },

     data(){
        return{
           blogs:[
               {
          id: 1,
          title: "My first blog post",
        //   icons: AiOutlineStar,
          text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur molestias voluptate mollitia officia beatae veniam optio aperiam! Vitae incidunt enim quod ad, perferendis aperiam iusto maiores earum quos obcaecati sunt.
          Obcaecati, unde in harum sit fuga eos odio neque .`,
          img: image1,
          isFavorite: false,
        },
        {
          id: 2,
          title: "My second blog post",
        //   icons: AiOutlineStar,
          text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur molestias voluptate mollitia officia beatae veniam optio aperiam! Vitae incidunt enim quod ad, perferendis aperiam iusto maiores earum quos obcaecati sunt.
          Obcaecati, unde in harum sit fuga eos odio n.`,
          img: image2,
          isFavorite: false,
        },
          {
         id: 3,
         title: "My third blog post",
        //  icons: AiOutlineStar,
         text: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur numquam eos delectus necessitatibus? Minima, aliquam, officia incidunt inventore veritatis obcaecati harum, rerum ab asperiores iste totam corporis alias accusantium eligendi.
         Eaque porro velit cumque reprehenderit. `,
         img:  image3,
         isFavorite: true,
      },
     {
         id: 4,
         title: "my fourth blog post",
        //  icons: AiOutlineStar,
         text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur molestias voluptate mollitia officia beatae veniam optio aperiam! Vitae incidunt enim quod ad, perferendis aperiam iusto maiores earum quos obcaecati sunt.
         Obcaecati, unde in harum sit .`,
        img: image4,
        isFavorite: true,
  },

 ]
}
     }


  }

</script>

<style>
  .blog-list{
  display: flex;

  flex-wrap: wrap;
  margin-left: 100px;
}

</style>