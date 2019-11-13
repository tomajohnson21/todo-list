<template>
    <div class="container">
        <app-todo-grid v-bind:todos="todos"></app-todo-grid>
    </div>
</template>

<script>
    import TodoGrid from './components/TodoGrid'

    export default {
        data: function() {
            return {
                todos: ["Test item 1", "Test item 2"],
                maxItems: 10
            }
        },
        components: {
            appTodoGrid: TodoGrid
        }
    }
</script>

<style>
</style>
