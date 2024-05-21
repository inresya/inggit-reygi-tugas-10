<template>
    <div>
      <h2>Todos</h2>
      <ul>
        <li v-for="todo in todos" :key="todo.id">{{ todo.title }}</li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Todos',
    data() {
      return {
        todos: [
          { id: 1, title: 'Learn Vue.js' },
          { id: 2, title: 'Build a project' }
        ]
      };
    }
  };
  </script>
  