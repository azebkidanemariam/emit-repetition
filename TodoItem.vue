<template>
  <li class="todo-item">
    {{todo.content}}
    <button @click="remove">Delete</button>
  </li>
</template>

<script>
export default {
  props: {
    todo: Object
  },

  methods: {
    remove(){
      this.$emit('deleteMe', this.todo.id)
    }
  }
}
</script>

<style>

</style>