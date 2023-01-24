<template>

  <div class="app">
    <post-form @create = "createPost"></post-form>
    <post-list v-bind:posts="posts"></post-list>
  </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {

  components:{
    PostForm, PostList,
  },

  data(){
    return{
      posts: [
        {id: 1, title: 'Java 1', body: '1 Java - язык программирования предназначенный для'},
        {id: 2, title: 'Java 2', body: '2 Java - язык программирования предназначенный для'},
        {id: 3, title: 'Java 3', body: '3 Java - язык программирования предназначенный для'},
      ]
    }
  },

  methods: {
      createPost(post){
          this.posts.push(post)
      },


  }
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}



form{
  display: flex;
  flex-direction: column;
}

.app{
  padding: 20px;
}



</style>