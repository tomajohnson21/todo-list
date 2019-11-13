<template>
  <div class="row">
    <app-todo-item 
      v-for="(todo, index) in todos" 
      v-bind:key="index" 
      @click.native="deleteItem(index)"
    >
      {{ todo }}
    </app-todo-item>
  </div>
  
</template>

<script>
  import TodoItem from './TodoItem'

  export default {
    props: ['todos'],
    methods: {
      deleteItem(index) {
        this.$emit('itemDeleted', index)
      }
    },
    components: {
      appTodoItem: TodoItem 
    }
  }
</script>

<style>

</style>