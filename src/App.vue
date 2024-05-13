<template>
  <div class="app">
    <post-form
    @create="creatPost"
    />
    <PostList 
    :posts="posts"
    
    />
  </div>

</template>

<script>
import PostForm from "./components/PostForm.vue";
import PostList from "./components/PostList.vue";
export default {
  components:{
    PostList,
    PostForm,
  },
  data(){
    return{
      posts: [
        {id:1, title: 'Пост1', body: 'Описание 1'},
        {id:2, title: 'Пост2', body: 'Описание 2'},
        {id:3, title: 'Пост3', body: 'Описание 3'},
      ],
    }
  },
  methods:{
    creatPost(post) {
      this.posts.push(post);
    },
  }
}
</script>

<style scoped>
*
{
  margin: 0;
  padding: 0;
  box-sizing: border-boxz;
}


.app{
  padding: 20px
}

</style>
