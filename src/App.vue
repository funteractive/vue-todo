<template>
  <div class="section">
    <div class="container">
      <h1>Todo App</h1>
      <Todo/>
    </div>
  </div>
</template>

<script>
import Todo from './components/Todo.vue'

export default {
  name: 'app',
  components: {
    Todo
  }
}
</script>

<style>
#app {
}
</style>
