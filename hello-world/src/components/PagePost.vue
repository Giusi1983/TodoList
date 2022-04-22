<template>
  <div class="PagePost d-sm-flex">
    <div v-bind:key="post.id" v-for="post in posts" id="container_post" class="container justify d-sm-flex col-4 p-6">
     <div class="card row" style="width: 350px; height:450px;">
      <div class="card-body">
        <div class="justify pr-55">
         <p>{{post.user_id}}</p>
          <h5>{{post.title}}</h5>
           <p>{{post.body}}</p>
         </div>
       </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PagePost',
  props: ["posts"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
