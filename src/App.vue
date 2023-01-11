<template>

  <div class="app">

      <form>
        <h4>Добавить пост</h4>
        <input class="input" type="text" placeholder="Название">
        <input class="input" type="text" placeholder="Описание">
        <button>Создать пост</button>
      </form>


  <div class="post" v-for="post in posts" :key="post.id">
      <div><strong>Название: </strong>{{post.title}}</div>
      <div><strong>Описание: </strong>{{post.body}}</div>
  </div>
  </div>

</template>

<script>

export default {
  data(){
    return{
      posts: [
        {id: 1, title: 'Java 1', body: '1 Java - язык программирования предназначенный для'},
        {id: 2, title: 'Java 2', body: '2 Java - язык программирования предназначенный для'},
        {id: 3, title: 'Java 3', body: '3 Java - язык программирования предназначенный для'},
      ]
    }
  },

  // methods: {
  //
  //
  // }
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.post{
  padding: 15px;
  border: 2px solid cornflowerblue;
  margin-top: 5px;
}

.input{
  width: 100%;
  border: 2px solid cornflowerblue;
  padding: 15px;
  margin-top: 5px;
}

.app{
  padding: 20px;
}

</style>