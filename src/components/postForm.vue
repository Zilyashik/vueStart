<template>
  <form @submit.prevent>
    <input
        :value="post.title"
        @input="post.title = $event.target.value"
        class="input"
        type="text"
        placeholder="Name">
    <input
        :value="post.body"
        @input="post.body = $event.target.value"
        class="input"
        type="text"
        placeholder="Description">
    <button
        class="btn"
        @click="createPost">Create</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  }
}
</script>

<style scoped>
.input{
  width: 100%;
  border: 2px solid lightskyblue;
  padding: 10px 15px;
  margin-top: 15px;
}
.btn{
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
</style>