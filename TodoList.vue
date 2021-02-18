<template>
  <ul class="todo-list">
    <TodoItem 
      v-for="item in todos" :key="item.id"
      :todo="item"
      v-on:deleteMe="deleteTodo"
    />
  </ul>
</template>

<script>
import TodoItem from './TodoItem'

export default {
  components: {TodoItem},
  props: {
    todos: Array
  },


  methods: {
    deleteTodo(todoId){
      this.$emit('deleteTodo', todoId)
    }
  }
}
</script>

<style>

</style>