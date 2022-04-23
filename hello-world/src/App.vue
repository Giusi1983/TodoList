<template>
  <div id="app">
    <dashboard-card
      title="Latest Posts"
      id="post-page" class="vs-con-loading_container"
      />
      <div class="w-full text-xl md:text-2x1 font-bold" id="page_container">
      <h2 to="/Post">Latest Posts</h2>
´    <PagePost title="Latest Posts" v-bind:posts="posts" />
    <h2 to="/Todos" class="mt-5">My Todos</h2>
 <ToDos title="My Todos" v-bind:todos="todos" class="d-sm-flex"/>
   </div>
  </div>
</template>

<script>
import PagePost from './components/PagePost.vue'; 
import ToDos from './components/ToDos.vue'; 
import axios from 'axios'; 

export default {
  name: 'App',
  components: {
    PagePost, 
    ToDos
  },
  data(){
    return {
      todos:[],
      posts: []
    }
  },
  created() {
     axios.get('https://gorest.co.in/public/v2/posts?_limit=2')
    .then(res => this.posts = res.data)
    .catch(err => console.log(err)); 
},
mounted() {
  axios.get('https://gorest.co.in/public/v2/todos?_limit=2')
    .then(res => this.todos = res.data)
    .catch(err => console.log(err));
 }
}
    
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#page_container {
  display:flex; 
  flex-direction: column;
  align-items: center;
}
</style>
