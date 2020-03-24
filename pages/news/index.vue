<template>
  <div>
    <h1>Berita</h1>
    <ul v-for="article in news" :key="article">
      <li>{{ article.title.rendered }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data: {
    news: [],
  },
  async asyncData({ $axios }) {
    const data = await $axios.$get('https://kawalcovid19.id/_next/data/eRnviEofSpR2YFgL9WIKA/index.json')
    let news = data.pageProps.information
    return { news: news }
  }
}
</script>

<style>

</style>
