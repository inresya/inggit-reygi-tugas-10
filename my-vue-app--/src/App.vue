<template>
  <div id="app">
    <header>
      <nav>
        <button @click="currentView = 'Todos'">Todos</button>
        <button @click="currentView = 'Posts'">Posts</button>
      </nav>
    </header>
    <component :is="currentView" />
  </div>
</template>

<script>
import Todos from './components/Todos.vue';
import Posts from './components/Posts.vue';

export default {
  name: 'App',
  components: {
    Todos,
    Posts
  },
  data() {
    return {
      currentView: 'Todos'
    };
  }
};
</script>

<style>
nav {
  display: flex;
  gap: 10px;
}
button {
  padding: 10px;
  cursor: pointer;
}
</style>
