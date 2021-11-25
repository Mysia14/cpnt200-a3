<template>
  <v-main>
    <header>
      <Header :title="info.title" :subHeading="info.tagline" />
    </header>
    <section>
      <h2>The beauty of the Seasons</h2>
      <ul>
        <li>{{ topics[0] }}</li>
        <li>{{ topics[1] }}</li>
        <li>{{ topics[2] }}</li>
      </ul>
    </section>
    <section>
      <h2>Credits</h2>
      <p>{{ references.name }}, {{ references.location }}</p>
    </section>
    <footer>
      <p>&copy; 2021 Mysia Santana</p>
    </footer>
  </v-main>
</template>

<script>
export default {
  data() {
    return {
      info: {
        title: "photos",
        author: "mysia",
        tagline: "the beautiful nature",
      },
      references: {
        name: "nature",
        location: "Canada",
      },
      topics: ["memories", "album", "stories"],
    };
  },
};
</script>