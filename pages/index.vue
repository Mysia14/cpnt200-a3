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
          <nuxt-link :to="`recipe/${recipe.slug}`">{{recipe.recipeName}}</nuxt-link>
        </li>
      </ul>
    </v-card>
  </nav>
</template>

<script>
export default { 
  //// fetch the data from the blog in the content folder
  async asyncData({ $content }) {
    const posts = await $content("gallery").fetch();
    const recipes = await $content("recipe").fetch();
    return {
      posts,
      recipes,
    };
  },
};
 
</script>