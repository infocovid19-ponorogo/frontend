<template>
  <div class="w-full mt-5">
    <div class="container mx-auto px-5">
      <div class="text-xl" v-if="category.name">{{ category.name }}</div>
      <h1 class="text-3xl font-bold max-w-xl">{{ article.title.rendered }}</h1>
      <div v-if="category.id == 2" class="text-lg max-w-xl" v-html="article.excerpt.rendered"></div>
      <div class="my-5 text-sm text-gray-600">
        Sumber artikel:
        <a class="block underline hover:text-blue-400" :href="`//kawalcovid19.id/content/${article.id}/${article.slug}`">https://kawalcovid19.id/content/{{ article.id }}/{{ article.slug }}</a>
      </div>
      <hr class="my-4" />
      <div class="mt-8">
        <div id="article-content" v-html="article.content.rendered"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: "home",
  async asyncData({ $axios, route, params }) {
    const article = await $axios.$get(
      `https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts/${params.id}`
    );
    const category = await $axios.$get(
      `https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/categories/${article.categories[0]}`
    );
    return { article, category };
  }
}
</script>

<style>
  #article-content {
    overflow-wrap: break-word;
    overflow: scroll;
  }
  #article-content h1{
    margin-bottom: 18px;
    font-size: 36px;
    line-height: 36px;
    font-weight: 600;
  }
  #article-content h2{
    margin-bottom: 16px;
    font-size: 32px;
    line-height: 36px;
    font-weight: 600;
  }
  #article-content h3{
    margin-bottom: 14px;
    font-size: 28px;
    line-height: 36px;
    font-weight: 600;
  }
  #article-content h4{
    margin-bottom: 12px;
    font-size: 24px;
    line-height: 36px;
    font-weight: 600;
  }
  #article-content h5{
    margin-bottom: 10px;
    font-size: 20px;
    line-height: 36px;
    font-weight: 600;
  }
  #article-content h6{
    margin-bottom: 8px;
    font-size: 14px;
    line-height: 36px;
    font-weight: 600;
  }
  #article-content p{
    line-height: 24px;
    margin-bottom: 16px;
  }
  #article-content ul{
    display: block;
    list-style-type: none;
    margin: 12px 12px 16px 16px;
    padding: 0px;
  }
  #article-content ul li{
    font-size: 16px;
    line-height: 24px;
    margin-bottom: 12px;
  }
  #article-content ul > li::before {
    content: "–";
    display: inline-block;
    color: rgb(102, 107, 115);
    position: absolute;
    margin-left: -15px;
  }
  #article-content .wp-block-table {
    overflow-x: auto;
  }
</style>
