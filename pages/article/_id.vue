<template>
  <div>
    <h1>Detail Artikel</h1>
    <p class="text-center">{{ article.title }}</p>
    <div class="flex justify-center">
      <img class="rounded-md" :src="article.img" alt="" width="300px" />
    </div>
    <p class="text-center">{{ article.content }}</p>
    <div class="flex justify-center mt-1">
      <a class="rounded-lg bg-gray-700 p-1 px-4 text-white" href="/">Back</a>
    </div>
  </div>
</template>

<script>
import { fetchArticleById } from '@/api/article'
export default {
  async asyncData({ params }) {
    const articleId = params.id
    const article = await fetchArticleById(articleId)

    return {
      article,
    }
  },
}
</script>
