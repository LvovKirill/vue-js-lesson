<template>
  <div>

    <h3>Список пользователей</h3>
    <post-item v-for="post in posts" :post="post" v-bind:key="post"/>

  </div>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
  components: {PostItem},
  props:{
    posts:{
      type: Array,
      required: true,
    }
  },
  name: "PostList"
}
</script>

<style scoped>

.post{
  padding: 15px;
  border: 2px solid cornflowerblue;
  margin-top: 5px;
}

</style>