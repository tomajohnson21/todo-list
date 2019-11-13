<template>
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
          <label>New Item</label>
          <textarea class="form-control" rows="3" v-model="newItem"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
          <button class="btn btn-primary" @click.prevent="createNew">Add Item</button>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
    data: function() {
      return {
        newItem: ''
      }
    },
    methods: {
      createNew() {
        this.$emit('itemAdded', this.newItem);
        this.newItem = '';
      }
    }
  }
</script>

<style scoped>

  .btn {
    margin-top: 10px;
    margin-bottom: 10px;
  }
</style>