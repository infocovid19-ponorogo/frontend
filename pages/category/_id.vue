<template>
  <div class="w-full mt-5">
    <div class="container mx-auto px-5">
      <h1 class="text-3xl font-bold">{{ category.name }}</h1>
      <p>Informasi terkini mengenai COVID-19. 100% faktual, dari sumber-sumber terpercaya.</p>

      <div class="list-article mt-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
          <div
            v-for="article in articles"
            :key="article.id"
            class="rounded-lg shadow p-6 bg-white mb-3"
          >
            <nuxt-link :to="`/info/${article.id}`" class="font-semibold text-lg hover:underline"><h3 >{{ article.title.rendered }}</h3></nuxt-link>
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
  async asyncData({ $axios, params }) {

    const articles = await $axios.$get(
      `https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=${params.id}`
    );
    const category = await $axios.$get(
      `https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/categories/${params.id}`
    );

    return { articles, category };
  }
};
</script>

<style>
</style>
