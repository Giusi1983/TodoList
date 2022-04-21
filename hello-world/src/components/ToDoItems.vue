<template>
 <div class="Todo container">
   <div class="todo-item container col md m-2 p-6" v-bind:class="{'is-complete': todo.completed}">
     <div class="card row">
        <div class="card-body">
          <div class="justify">
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
