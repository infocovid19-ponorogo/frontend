<template>
  <div class="w-full ">
    <div class="container mx-auto px-5 pt-32">
      <h3 class="font-bold text-4xl max-w-xl text-gray-800">Informasi seputar COVID-19 di Ponorogo secara tepat dan akurat.</h3>
      <p class="text-xl text-gray-800">Situs ini merupakan sumber informasi inisiatif sukarela warganet Ponorogo yang pro-data.</p>
      <div class="container mt-12">
        <h3 class="font-semibold text-2xl mt-10 mb-5">Jumlah Kasus di Ponorogo Saat Ini</h3>
        <div class="flex flex-col lg:flex-row justify-between mb-4 lg:mb-8">
          <div class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8">
            <div class="text-6xl font-bold text-orange-400 numeric">{{ dtPonorogo.summary.positif_total }}</div>
            <div class="text-xl text-gray-800">Positif</div>
          </div>
          <div class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8">
            <div class="text-6xl font-bold text-green-400 numeric">{{ dtPonorogo.summary.sembuh_total }}</div>
            <div class="text-xl">Sembuh</div>
          </div>
          <div class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8">
            <div class="text-6xl font-bold text-red-400 numeric">{{ dtPonorogo.summary.meninggal_total }}</div>
            <div class="text-xl">Meninggal</div>
          </div>
        </div>

        <div class="flex flex-col lg:flex-row justify-between">
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div class="text-5xl font-semibold text-blue-400 numeric">{{ dtPonorogo.summary.odr_total }}</div>
            <div class="text-xl">Orang Dalam Resiko (ODR)</div>
          </div>
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div class="text-5xl font-semibold text-blue-400 numeric">{{ dtPonorogo.summary.odp_total }}</div>
            <div class="text-xl">Orang Dalam Pemantuan (ODP)</div>
          </div>
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div class="text-5xl font-semibold text-blue-400 numeric">{{ dtPonorogo.summary.pdp_total }}</div>
            <div class="text-xl">Pasien Dalam Pemantuan (PDP)</div>
          </div>
        </div>

        <div class="lg:my-4 text-sm">
          <p class="font-mono">Pembaruan terakhir: 25 Maret 2020</p>
          <p class="font-sans">Sumber: <span class="italic">Dinas Kesahatan Kabupaten Ponorogo</span></p>
        </div>

        <h3 class="font-semibold text-2xl mt-10 mb-5">Jumlah Kasus di Indonesia dan Provinsi Jawa Timur</h3>
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
          <p class="font-mono">Pembaruan terakhir: {{ dtIndo.metadata.lastUpdatedAt }}</p>
          <p class="font-sans">Sumber: <span class="italic">https://kawalcovid19.id/</span></p>
        </div>

         <div class="p-5 mt-4 md:mt-12 md:p-8 rounded-lg" style="background-color:#63b3ed">
          <h3 class="text-xl lg:text-2xl text-white"><strong>Ketahui Resiko dari COVID-19</strong></h3>
          <br>
          <div class="flex flex-col lg:flex-row justify-between items-start">
              <p class="text-white text-lg w-full lg:w-2/3">
                  COVID-19 merupakan penyakit yang disebabkan Novel Coronavirus 2019. Meski bergejala mirip dengan flu biasa, COVID-19 sampai saat ini memiliki fatalitas lebih tinggi. Virus ini juga menyebar dengan sangat cepat karena bisa pindah dari orang ke orang bahkan sebelum orang tersebut tidak menunjukkan gejala.
                  <br>
                  <br> Penting bagi Anda untuk menilai kondisi secara mandiri. Anda bergejala?
              </p> <i style="flex:0 0 2rem"></i> <a href="https://checkupcovid19.jatimprov.go.id/covid19/#!/checkup/" target="_blank" class="px-10 py-4 rounded-lg text-white border-2 border-solid border-white hover:bg-brand-green-light"><b>Nilai Diri Saya</b></a></div>
          </div>
      </div>

         <h3 class="font-semibold text-2xl mt-10 mb-5">Info Terkini</h3>
        <div class="list-article">
          <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
            <div v-for="article in articlesInfoTerkini" :key="article.id" class="rounded-lg shadow p-6 bg-white mb-3">
              <h3 class="font-semibold text-lg">{{ article.title.rendered }}</h3>
              <div v-if="article.excerpt.rendered" v-html="article.excerpt.rendered"></div>
            </div>
          </div>
          <div class="py-5 text-center">
            <a class="text-blue-400 p-4 rounded border-2 border-blue-300 font-bold text-sm" href="">Lihat Semua Berita</a>
          </div>
        </div>

        <h3 class="font-semibold text-2xl mt-10 mb-5">Periksa Fakta</h3>
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

         <h3 class="font-semibold text-2xl mt-10 mb-5">Tips dan Infografik Terbaru</h3>
        <div class="list-article">
          <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
            <div v-for="article in articlesInfoGrafik" :key="article.id" class="rounded-lg shadow p-6 bg-white mb-3">
              <h3 class="font-semibold text-lg">{{ article.title.rendered }}</h3>
            
            </div>
          </div>
          <div class="py-5 text-center">
            <a class="text-blue-400 p-4 rounded border-2 border-blue-300 font-bold text-sm" href="">Lihat Semua Berita</a>
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
    const articles = await $axios.$get('https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=12')
     const dtPonorogo = await $axios.$get('https://api.infocovid19ponorogo.id/api/kecamatan')
         const articlesInfoTerkini = await $axios.$get('https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=2')
      const articlesInfoGrafik = await $axios.$get('https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=19')

    return { dtIndo, articles,dtPonorogo,articlesInfoGrafik,articlesInfoTerkini }
  }
}
</script>

<style>
  .numeric {
    font-family: 'Fjalla One';
  }
</style>
