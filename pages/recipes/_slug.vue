<template>
  <v-main>
    <v-container>
      <h2>#1 {{ post.title }}</h2>
      <nuxt-content :document="post" />
    </v-container>
    <v-container>
      <h2>#2 {{ post.title }}</h2>
      <p>{{ post.description }}</p>
      <nuxt-content :document="post" />

      <p>Published date: {{ post.date }}</p>
    </v-container>
  </v-main>
</template>
<script>
export default {
  async asyncData({ $content, params, error }) {
    try {
      const post = await $content(`blog/${params.slug}`).fetch()
      return {
        post,
      }
    } catch (e) {
      error('No article found')
    }
  },
}
</script>