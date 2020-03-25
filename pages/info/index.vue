<template>
  <div class="w-full">
    <div class="container mx-auto px-5">
      <h1 class="text-3xl font-bold">Informasi Terkini</h1>
      <p>Informasi terkini mengenai COVID-19. 100% faktual, dari sumber-sumber terpercaya.</p>

      <div class="list-article mt-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
          <div
            v-for="article in articlesInfoTerkini"
            :key="article.id"
            class="rounded-lg shadow p-6 bg-white mb-3"
          >
            <a :href="`info/${article.id}`" class="font-semibold text-lg hover:underline"><h3 >{{ article.title.rendered }}</h3></a>
            <div v-if="article.excerpt.rendered" v-html="article.excerpt.rendered"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  layout: "home",
  async asyncData({ $axios }) {
    const articles = await $axios.$get(
      "https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=12"
    );
    const articlesInfoTerkini = await $axios.$get(
      "https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=2"
    );
    const articlesInfoGrafik = await $axios.$get(
      "https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=19"
    );

    return { articles, articlesInfoGrafik, articlesInfoTerkini };
  }
};
</script>

<style>
</style>
