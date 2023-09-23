<template>
  <div class="container mx-auto">
    <h1>Daftar Artikel</h1>
    <ul>
      <li v-for="article in articles" :key="article.id">
        <nuxt-link :to="'/article/' + article.id">{{
          article.title
        }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        { id: 1, title: 'Artikel 1' },
        { id: 2, title: 'Artikel 2' },
        { id: 3, title: 'Artikel 3' },
      ],
    }
  },
}
</script>
