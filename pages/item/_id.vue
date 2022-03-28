<template>
  <div>
    <h1>URL Param</h1>
    <h2>User ID : {{ this.$route.params.id }}</h2>

    <div>
      <div>count : {{ this.$store.state.count }}</div>
      <button @click="increment">追加</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    increment() {
      this.$store.commit(
        'increment', {amount: Number(this.$route.params.id)}
      )
    }
  }
}
</script>
