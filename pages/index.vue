<template>
  <nav>
    <h2>A Beautiful Gallery</h2>
    <v-card>
      <ul>
        <li v-for="post in posts" :key="post.slug">
          <nuxt-link :to="`gallery/${post.slug}`">{{ post.title }}</nuxt-link>
        </li>
      </ul>
    </v-card>
    <h2>Four Seasons</h2>
    <v-card>
      <ul>
        <li v-for="recipe in recipes" :key="recipe.slug">
          <nuxt-link :to="`recipe/${recipe.slug}`">{{
            recipe.recipeName
          }}</nuxt-link>
        </li>
      </ul>
    </v-card>
  </nav>
</template>

<script>
export default { 
  //// fetch the data from the blog in the content folder
  async asyncData ({ $content, params }) {
    const posts = await $content('blog').fetch();
    const recipes = await $content('recipe').fetch();
    return {
      posts,
      recipes,
    }
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' },
      ],
    }
  },
}
</script>