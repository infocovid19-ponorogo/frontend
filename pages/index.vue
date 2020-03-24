<template>
  <div class="w-full ">
    <div class="container mx-auto px-5 pt-32">
      <h1 class="font-bold text-4xl max-w-xl text-gray-800">Kawal informasi seputar COVID-19 secara tepat dan akurat.</h1>
      <p class="text-xl text-gray-800">Situs ini merupakan sumber informasi inisiatif sukarela warganet Indonesia pro-data, terdiri dari praktisi kesehatan, akademisi & profesional.</p>
      <div class="container mt-12">
        <h3 class="font-semibold text-2xl mt-10 mb-5">Jumlah Kasus di Ponorogo Saat Ini</h3>
        <div class="flex flex-col lg:flex-row justify-between mb-4 lg:mb-8">
          <div class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8">
            <div class="text-6xl font-bold text-orange-400 numeric">0</div>
            <div class="text-xl text-gray-800">Positif</div>
          </div>
          <div class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8">
            <div class="text-6xl font-bold text-green-400 numeric">0</div>
            <div class="text-xl">Sembuh</div>
          </div>
          <div class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8">
            <div class="text-6xl font-bold text-red-400 numeric">0</div>
            <div class="text-xl">Meninggal</div>
          </div>
        </div>

        <div class="flex flex-col lg:flex-row justify-between">
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div class="text-5xl font-semibold text-blue-400 numeric">864</div>
            <div class="text-xl">Orang Dalam Resiko (ODR)</div>
          </div>
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div class="text-5xl font-semibold text-blue-400 numeric">57</div>
            <div class="text-xl">Orang Dalam Pemantuan (ODP)</div>
          </div>
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div class="text-5xl font-semibold text-blue-400 numeric">6</div>
            <div class="text-xl">Pasien Dalam Pemantuan (PDP)</div>
          </div>
        </div>

        <div class="lg:my-4 text-sm">
          <p class="font-mono">Pembaruan terakhir: 23 Maret 2020</p>
          <p class="font-sans">Sumber: <span class="italic">Dinas Kesahatan Kabupaten Ponorogo</span></p>
        </div>

        <h3 class="font-semibold text-2xl mt-10 mb-5">Jumlah Kasus di Indonesia dan Provinsi</h3>
        <div class="flex flex-col lg:flex-row">
          <div class="w-full lg:w-1/3 bg-white lg:border-r lg:mb-0 mb-4 p-6">
            <div class="text-2xl font-semibold text-orange-400 my-2">Terkonfirmasi</div>
            <hr>
            <div class="flex justify-between mt-4">
              <div class="font-semibold">Jawa Timur</div>
              <div class=" text-2xl font-semibold text-gray-700 numeric">51</div>
            </div>
            <div class="flex justify-between">
              <div class="font-semibold">Indonesia</div>
              <div class=" text-2xl font-semibold text-gray-700 numeric">{{ dtIndo.confirmed.value }}</div>
            </div>
          </div>
          <div class="w-full lg:w-1/3 bg-white lg:border-r lg:mb-0 mb-4 p-6">
            <div class="text-2xl font-semibold text-green-500 my-2">Sembuh</div>
            <hr>
            <div class="flex justify-between mt-4">
              <div class="font-semibold">Jawa Timur</div>
              <div class=" text-2xl font-semibold text-gray-700 numeric">0</div>
            </div>
            <div class="flex justify-between">
              <div class="font-semibold">Indonesia</div>
              <div class=" text-2xl font-semibold text-gray-700 numeric">{{ dtIndo.recovered.value }}</div>
            </div>
          </div>
          <div class="w-full lg:w-1/3 bg-white lg:mb-0 mb-4 p-6">
            <div class="text-2xl font-semibold text-red-500 my-2">Meninggal</div>
            <hr>
            <div class="flex justify-between mt-4">
              <div class="font-semibold">Jawa Timur</div>
              <div class=" text-2xl font-semibold text-gray-700 numeric">1</div>
            </div>
            <div class="flex justify-between">
              <div class="font-semibold">Indonesia</div>
              <div class=" text-2xl font-semibold text-gray-700 numeric">{{ dtIndo.deaths.value }}</div>
            </div>
          </div>
        </div>

        <div class="lg:my-4 text-sm">
          <p class="font-mono">Pembaruan terakhir: 23 Maret 2020</p>
          <p class="font-sans">Sumber: <span class="italic">https://kawalcovid19.id/</span></p>
        </div>

        <h3 class="font-semibold text-2xl mt-10 mb-5">Informasi Terkini</h3>
        <div class="list-article">
          <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
            <div v-for="article in articles" :key="article.id" class="rounded-lg shadow p-6 bg-white mb-3">
              <h3 class="font-semibold text-lg">{{ article.title.rendered }}</h3>
              <div v-if="article.excerpt.rendered" v-html="article.excerpt.rendered"></div>
            </div>
          </div>
          <div class="py-5 text-center">
            <a class="text-blue-400 p-4 rounded border-2 border-blue-300 font-bold text-sm" href="">Lihat Semua Berita</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'home',
  async asyncData({ $axios }) {
    const dtIndo = await $axios.$get('https://kawalcovid19.harippe.id/api/summary')
    const articles = await $axios.$get('https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts')

    return { dtIndo, articles }
  }
}
</script>

<style>
  .numeric {
    font-family: 'Fjalla One';
  }
</style>
