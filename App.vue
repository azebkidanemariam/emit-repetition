<template>
  <div class="wrapper">
    <TodoList :todos="todos" v-on:deleteTodo="deleteTodo"/>
  </div>
</template>

<script>
import TodoList from './TodoList'

export default {
  components: {TodoList},
  data(){return {
    todos: [
      {id: 4, content: "Köp mjölk", done: false},
      {id: 8, content: "Köpa semla<3", done: false},
      {id: 16, content: "Åka skriskor", done: false},
      {id: 1337, content: "Köp choklad", done: false},
    ]
  }},

  methods: {
    deleteTodo(todoId){
      this.todos = this.todos.filter( element => element.id != todoId)
    }
  }
}
</script>

<style>

</style>