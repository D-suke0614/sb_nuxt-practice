<template>
  <div>
    <h1>User List</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{ post.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const posts = await $axios.$get(
      'https://jsonplaceholder.typicode.com/users/'
    )
    return{ posts }
  }
}
</script>
