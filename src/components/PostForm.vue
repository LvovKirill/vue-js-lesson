<template>
  <form @submit.prevent>
    <h4>Добавить пост</h4>
    <input v-model="post.title" class="input" type="text" placeholder="Название">
    <input v-model="post.body" class="input" type="text" placeholder="Описание">
    <button @click="createPost" class="btn">Создать пост</button>
  </form>
</template>

<script>
export default {

  data(){
    return{
      post: {
        title: '',
        body: '',

      }
    }
  },

  methods:{
    createPost(){
      this.post.id = Date.now();
      this.$emit('create', this.post)
      this.post = {
        title: '',
        body: '',
      }
    }
  },

  name: "PostForm"
}
</script>

<style scoped>

.input{
  width: 100%;
  border: 2px solid cornflowerblue;
  padding: 15px;
  margin-top: 5px;
}

.btn{
  margin-top: 5px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: cornflowerblue;
  border: 1px solid cornflowerblue;
}

</style>