<template>
    <div class="container">
        <app-header></app-header>
        <app-new-item @itemAdded="newItem"></app-new-item>
        <app-todo-grid v-bind:todos="todos" @itemDeleted="deleteItem"></app-todo-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Click on an item to delete it</div>
            </div>
        </div>
    </div>
</template>

<script>
    import TodoGrid from './components/TodoGrid'
    import NewItem from './components/NewItem'
    import Header from './components/Header'

    export default {
        data: function() {
            return {
                todos: ["Test item 1", "Test item 2"],
                maxItems: 10
            }
        },
        methods: {
            newItem(item) {
                this.todos.push(item);
            },
            deleteItem(index) {
                this.todos.splice(index, 1);
            }
        },
        components: {
            appTodoGrid: TodoGrid,
            appNewItem: NewItem,
            appHeader: Header
        }
    }
</script>

<style>
</style>
