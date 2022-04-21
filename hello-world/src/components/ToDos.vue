<template>
  <div>
    <div v-bind:key="todo.id" v-for="todo in todos">
    <ToDoItems v-bind:todo="todo"/>
  </div>
  </div>
</template>

<script>
import ToDoItems from './ToDoItems.vue'
export default {
  name: 'ToDos',
  props: ["todos"], 
  components: {
    ToDoItems
 }
}
</script>
