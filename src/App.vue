<template>
  <div id="app">
    <Todos
      :todos="todos"
      @del-todo="delTodo"
    />
  </div>
</template>

<script>
import Todos from './components/Todos';

export default {
  data () {
      return {
          todos: [
              {
                  id: 1,
                  title: 'Todo One',
                  completed: false
              },
              {
                  id: 2,
                  title: 'Todo Two',
                  completed: true
              },
              {
                  id: 3,
                  title: 'Todo Three',
                  completed: false
              }
          ]
      }
  },
  components: {
      Todos
  },
  methods: {
      delTodo (id) {
          this.todos = this.todos.filter(todo => todo.id !== id);
      }
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
    line-height: 1.4;
  }

</style>
