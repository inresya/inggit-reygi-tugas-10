<template>
  <div>
    <h2>Posts</h2>
    <select v-model="selectedUser" @change="fetchPosts">
      <option v-for="user in users" :key="user.id" :value="user.id">
        {{ user.name }}
      </option>
    </select>
    <ul>
      <li v-for="post in posts" :key="post.id">{{ post.title }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Posts',
  data() {
    return {
      selectedUser: null,
      users: [
        { id: 1, name: 'User 1' },
        { id: 2, name: 'User 2' }
      ],
      posts: []
    };
  },
  methods: {
    fetchPosts() {
      // Fetch posts based on selectedUser
      // This is just dummy data
      const allPosts = {
        1: [
          { id: 1, title: 'Post 1 from User 1' },
          { id: 2, title: 'Post 2 from User 1' }
        ],
        2: [
          { id: 3, title: 'Post 1 from User 2' },
          { id: 4, title: 'Post 2 from User 2' }
        ]
      };
      this.posts = allPosts[this.selectedUser] || [];
    }
  }
};
</script>
