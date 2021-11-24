<template>
  <v-main>
    <article>
      <h2>{{ post.recipeName }}</h2>
      <p>{{ post.chef }}</p>
      <nuxt-img :src="post.image" sizes="sm:100vw md:50vw lg:600px" />
      <nuxt-content :document="post" />
    </article>
  </v-main>
</template>
<script>
export default {
  async asyncData({ $content, params, error }) {
    try {
      const post = await $content(`recipe/${params.slug}`).fetch();
      return {
        post,
      };
    } catch (error) {
      error(" Soryy! No article found");
    }
  },
};