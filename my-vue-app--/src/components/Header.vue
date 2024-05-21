<template>
    <header>
      <nav>
        <button @click="$emit('navigate', 'todos')">Todos</button>
        <button @click="$emit('navigate', 'posts')">Posts</button>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Header'
  };
  </script>
  
  <style scoped>
  nav {
    display: flex;
    gap: 10px;
  }
  button {
    padding: 10px;
    cursor: pointer;
  }
  </style>
  