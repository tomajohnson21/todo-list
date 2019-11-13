<template>
  <div class="col-sm-6 col-med-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body todo-item">
        <slot></slot>
      </div>
    </div>
  </div>
  
</template>

<script>
  export default {
    props: ['quotes']
  }
</script>

<style>
  .panel-body {
    font-size: 24px;
    color: #36454f;
  }

  .todo-item {
    cursor: pointer;
  }

  .todo-item:hover {
    background-color: #dc222e
  }
</style>