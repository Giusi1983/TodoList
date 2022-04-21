<template>
  <div class="todo-item" v-bind:class="{'is-complete': todo.completed}">
    <div class="row">
     <div class="col-sm-3">
       <div class="card">
        <div class="card-body">
         <p>
         <input type="checkbox">
           {{todo.id}}
         </p>
      <p>
      {{todo.title}}
     </p>
    <p>
      {{todo.status}}
    </p>
  </div>
  </div>
  </div>
  </div>
  </div>
</template>
<script>
export default {
  name:"TodoItem",
  props: ["todo"]
}
</script>
