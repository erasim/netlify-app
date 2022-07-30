<script>
export default {
  data: () => ({
    joke: '',
  }),
  async mounted() {
    this.joke = await fetch('https://jsonplaceholder.typicode.com/todos/1).then((res) => res.json())
  },
}
</script>

<template>
  <article>
    <blockquote>
      <p>{{ joke }}</p>
    </blockquote>
  </article>
</template>

<style scoped>
blockquote {
  border-left: 5px solid #ccc;
  padding: 0.5rem;
}
</style>
