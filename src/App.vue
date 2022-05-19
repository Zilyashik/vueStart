<template>
  <div class="app">
    <post-form/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>
import postForm from "@/components/postForm";
import postList from "@/components/postList";
  export default {
    components: {
      postList, postForm
    },
    data() {
      return {
        posts: [
          {id: 1, title: 'JavaScript', body: 'Post`s description'},
          {id: 2, title: 'JavaScript 2', body: 'Post`s description 2'},
          {id: 3, title: 'JavaScript 3', body: 'Post`s description 3'},
          {id: 4, title: 'JavaScript 4', body: 'Post`s description 4'},
        ],
        title: '',
        body: '',
      }
    },
    methods: {
      createPost() {
        const newPost = {
          id: Date.now(),
          title: this.title,
          body: this.body,
        }
        this.posts.push(newPost);
        this.title = '';
        this.body = '';
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
 .app{
   padding: 20px;
 }
 form{
   display: flex;
   flex-direction: column;
 }

</style>