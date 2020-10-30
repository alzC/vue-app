<template>
     <div id="app">
    <List/>
  </div>
</template>

<script>
import Todos from './components/Todos'
import List from './components/List.vue'
export default {

  data() {
      return {
        todos: [{ 
          name: 'Demo',
          completed: false
        }]
      }
  },
  methods: {
    addTodo () {
      this.todos.push({
        name: 'Jean',
        completed: false 
      })
    }
  },
  components: {
    Todos, List
  }
}
</script>


