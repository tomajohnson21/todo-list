<template>
  <div class="row">
    <app-todo-item v-for="todo in todos" v-bind:key="todo.index">
      {{ todo }}
    </app-todo-item>
  </div>
  
</template>

<script>
  import TodoItem from './TodoItem'

  export default {
    props: ['todos'],
    components: {
      appTodoItem: TodoItem 
    }
  }
</script>

<style>

</style>