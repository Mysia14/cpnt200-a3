<template>
  <v-main>
    <header>
      <Header :title="info.title" :subHeading="info.author" />
    </header>
    <section>
      <h2>My Gallery</h2>
      <p>here are some recipes I make</p>
      <ul>
        <li>{{ topics[0] }}</li>
        <li>{{ topics[1] }}</li>
        <li>{{ topics[2] }}</li>
      </ul>
    </section>
    <section>
      <h2>Memories</h2>
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
        title: "food stuff",
        author: "mysia",
        tagline: "beautiful memories",
      },
      references: {
        name: "Album",
        location: "Calgary",
      },
      topics: ["Canada", "immigration", "photos"],
    };
  },
};
</script>