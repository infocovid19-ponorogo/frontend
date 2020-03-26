<template>
  <div class="w-full">
    <div class="container mx-auto px-5">
      <!-- <h3 class="font-bold text-4xl max-w-xl text-gray-800">Informasi seputar COVID-19 di Ponorogo secara tepat dan akurat.</h3>
      <p class="text-xl text-gray-800">Situs ini merupakan sumber informasi inisiatif sukarela warganet Ponorogo yang pro-data.</p>-->
      <div class="flex lg:flex-row flex-col mt-5">
        <div class="lg:w-1/2 w-full bg-blue-400 rounded-lg">
          <div class="max-w-sm mx-auto py-24">
            <img class="h-20 w-full" src="~/assets/icon.svg" />
            <h3
              class="font-semibold text-white text-center mt-3"
            >Situs ini merupakan sumber informasi inisiatif sukarela warganet Ponorogo yang pro-data.</h3>
          </div>
        </div>
        <div class="lg:w-1/2 w-full flex flex-col lg:ml-4 lg:mt-0 mt-5">
          <a class="p-4 rounded-lg shadow-lg mb-2 bg-white" href="tel:119">
            <div class="block font-semibold">Call center Ponorogo</div>
            <div class="block text-xs">Nomor Darurat</div>
            <div class="flex flex-row text-blue-400 mt-5">
              <svg
                class="mr-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                width="24"
                height="24"
              >
                <path
                  class="heroicon-ui"
                  d="M13.04 14.69l1.07-2.14a1 1 0 0 1 1.2-.5l6 2A1 1 0 0 1 22 15v5a2 2 0 0 1-2 2h-2A16 16 0 0 1 2 6V4c0-1.1.9-2 2-2h5a1 1 0 0 1 .95.68l2 6a1 1 0 0 1-.5 1.21L9.3 10.96a10.05 10.05 0 0 0 3.73 3.73zM8.28 4H4v2a14 14 0 0 0 14 14h2v-4.28l-4.5-1.5-1.12 2.26a1 1 0 0 1-1.3.46 12.04 12.04 0 0 1-6.02-6.01 1 1 0 0 1 .46-1.3l2.26-1.14L8.28 4z"
                />
              </svg>
              <span class="text-lg font-bold">(0352) 3592999</span>
            </div>
          </a>
          <a class="p-4 rounded-lg shadow-lg mb-2 bg-white" href="tel:1500117">
            <div class="block font-semibold">Pemprov Jatim</div>
            <div class="block text-xs">Call Center</div>
            <div class="flex flex-row text-blue-400 mt-5">
              <svg
                class="mr-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                width="24"
                height="24"
              >
                <path
                  class="heroicon-ui"
                  d="M13.04 14.69l1.07-2.14a1 1 0 0 1 1.2-.5l6 2A1 1 0 0 1 22 15v5a2 2 0 0 1-2 2h-2A16 16 0 0 1 2 6V4c0-1.1.9-2 2-2h5a1 1 0 0 1 .95.68l2 6a1 1 0 0 1-.5 1.21L9.3 10.96a10.05 10.05 0 0 0 3.73 3.73zM8.28 4H4v2a14 14 0 0 0 14 14h2v-4.28l-4.5-1.5-1.12 2.26a1 1 0 0 1-1.3.46 12.04 12.04 0 0 1-6.02-6.01 1 1 0 0 1 .46-1.3l2.26-1.14L8.28 4z"
                />
              </svg>
              <span class="text-lg font-bold">1500117</span>
            </div>
          </a>
          <a class="p-4 rounded-lg shadow-lg mb-2 bg-white" href="tel:081335909288">
            <div class="block font-semibold">Dinkes Ponorogo</div>
            <div class="block text-xs">Hotline Corona</div>
            <div class="flex flex-row text-blue-400 mt-5">
              <svg
                class="mr-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                width="24"
                height="24"
              >
                <path
                  class="heroicon-ui"
                  d="M13.04 14.69l1.07-2.14a1 1 0 0 1 1.2-.5l6 2A1 1 0 0 1 22 15v5a2 2 0 0 1-2 2h-2A16 16 0 0 1 2 6V4c0-1.1.9-2 2-2h5a1 1 0 0 1 .95.68l2 6a1 1 0 0 1-.5 1.21L9.3 10.96a10.05 10.05 0 0 0 3.73 3.73zM8.28 4H4v2a14 14 0 0 0 14 14h2v-4.28l-4.5-1.5-1.12 2.26a1 1 0 0 1-1.3.46 12.04 12.04 0 0 1-6.02-6.01 1 1 0 0 1 .46-1.3l2.26-1.14L8.28 4z"
                />
              </svg>
              <span class="text-lg font-bold">081-335-909-288</span>
            </div>
          </a>
        </div>
      </div>

      <div class="container mt-12">
        <h3 class="font-semibold text-2xl mt-10 mb-5">Jumlah Kasus di Ponorogo Saat Ini</h3>
        <div class="flex flex-col lg:flex-row justify-between mb-4 lg:mb-8">
          <div
            class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8"
          >
            <div
              class="text-6xl font-bold text-orange-400 numeric"
            >{{ (dtPonorogo.summary) ? dtPonorogo.summary.positif_total: '_' }}</div>
            <div class="text-xl text-gray-800">Positif</div>
          </div>
          <div
            class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8"
          >
            <div
              class="text-6xl font-bold text-green-400 numeric"
            >{{ (dtPonorogo.summary) ? dtPonorogo.summary.sembuh_total: '_' }}</div>
            <div class="text-xl">Sembuh</div>
          </div>
          <div
            class="p-4 rounded text-center bg-white shadow lg:shadow-lg w-full lg:w-1/3 mb-4 lg:mb-0 lg:mr-8"
          >
            <div
              class="text-6xl font-bold text-red-400 numeric"
            >{{ (dtPonorogo.summary) ? dtPonorogo.summary.meninggal_total: '_' }}</div>
            <div class="text-xl">Meninggal</div>
          </div>
        </div>

        <div class="flex flex-col lg:flex-row justify-between">
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div
              class="text-5xl font-semibold text-blue-400 numeric"
            >{{ (dtPonorogo.summary) ? dtPonorogo.summary.odr_total: '_' }}</div>
            <div class="text-xl">Orang Dalam Resiko (ODR)</div>
          </div>
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div
              class="text-5xl font-semibold text-blue-400 numeric"
            >{{ (dtPonorogo.summary) ? dtPonorogo.summary.odp_total: '_' }}</div>
            <div class="text-xl">Orang Dalam Pemantuan (ODP)</div>
          </div>
          <div class="rounded shadow lg:shadow-lg bg-white lg:w-1/2 mb-4 lg:mb-0 lg:mr-8 p-6">
            <div
              class="text-5xl font-semibold text-blue-400 numeric"
            >{{ (dtPonorogo.summary) ? dtPonorogo.summary.pdp_total: '_' }}</div>
            <div class="text-xl">Pasien Dalam Pemantuan (PDP)</div>
          </div>
        </div>

        <div class="lg:my-4 text-sm">
          <p
            class="font-mono"
          >Pembaruan terakhir: {{(dtPonorogo.summary) ? dtPonorogo.summary.last_update_at: '_'}}</p>
          <p class="font-sans">
            Sumber:
            <span class="italic">Dinas Kesahatan Kabupaten Ponorogo</span>
          </p>
        </div>

        <h3
          class="font-semibold text-2xl mt-10 mb-5"
        >Jumlah Kasus di Indonesia dan Provinsi Jawa Timur</h3>
        <div class="flex flex-col lg:flex-row">
          <div class="w-full lg:w-1/3 bg-white lg:border-r lg:mb-0 mb-4 p-6">
            <div class="text-2xl font-semibold text-orange-400 my-2">Terkonfirmasi</div>
            <hr />
            <div class="flex justify-between mt-4">
              <div class="font-semibold">Jawa Timur</div>
              <div
                class="text-2xl font-semibold text-gray-700 numeric"
              >{{ (dtProv.attributes) ? dtProv.attributes.Kasus_Posi : '_' }}</div>
            </div>
            <div class="flex justify-between">
              <div class="font-semibold">Indonesia</div>
              <div
                class="text-2xl font-semibold text-gray-700 numeric"
              >{{ (dtIndo) ? dtIndo.positif : '_' }}</div>
            </div>
          </div>
          <div class="w-full lg:w-1/3 bg-white lg:border-r lg:mb-0 mb-4 p-6">
            <div class="text-2xl font-semibold text-green-500 my-2">Sembuh</div>
            <hr />
            <div class="flex justify-between mt-4">
              <div class="font-semibold">Jawa Timur</div>
              <div
                class="text-2xl font-semibold text-gray-700 numeric"
              >{{ (dtProv.attributes) ? dtProv.attributes.Kasus_Semb : '_' }}</div>
            </div>
            <div class="flex justify-between">
              <div class="font-semibold">Indonesia</div>
              <div
                class="text-2xl font-semibold text-gray-700 numeric"
              >{{ (dtIndo) ? dtIndo.sembuh : '_' }}</div>
            </div>
          </div>
          <div class="w-full lg:w-1/3 bg-white lg:mb-0 mb-4 p-6">
            <div class="text-2xl font-semibold text-red-500 my-2">Meninggal</div>
            <hr />
            <div class="flex justify-between mt-4">
              <div class="font-semibold">Jawa Timur</div>
              <div
                class="text-2xl font-semibold text-gray-700 numeric"
              >{{ (dtProv.attributes) ? dtProv.attributes.Kasus_Meni : '_' }}</div>
            </div>
            <div class="flex justify-between">
              <div class="font-semibold">Indonesia</div>
              <div
                class="text-2xl font-semibold text-gray-700 numeric"
              >{{ (dtIndo) ? dtIndo.meninggal : '_' }}</div>
            </div>
          </div>
        </div>
        <div class="lg:my-4 text-sm">
          <p class="font-sans">
            Sumber:
            <span class="italic">
              <a href="https://kawalcorona.com/">https://kawalcorona.com/</a>
            </span>
          </p>
        </div>

        <div class="bg-blue-400 p-5 mt-4 md:mt-12 md:p-8 rounded-lg">
          <h3 class="text-xl lg:text-2xl text-white">
            <strong>Ketahui Resiko dari COVID-19</strong>
          </h3>
          <br />
          <div class="flex flex-col lg:flex-row justify-between items-start">
            <p class="text-white text-lg w-full lg:w-2/3">
              COVID-19 merupakan penyakit yang disebabkan Novel Coronavirus 2019. Meski bergejala mirip dengan flu biasa, COVID-19 sampai saat ini memiliki fatalitas lebih tinggi. Virus ini juga menyebar dengan sangat cepat karena bisa pindah dari orang ke orang bahkan sebelum orang tersebut tidak menunjukkan gejala.
              <br />
              <br />Penting bagi Anda untuk menilai kondisi secara mandiri. Anda bergejala?
            </p>
            <i style="flex:0 0 2rem"></i>
            <nuxt-link
              to="https://checkupcovid19.jatimprov.go.id/covid19/#!/checkup/"
              target="_blank"
              class="px-10 py-4 rounded-lg text-white border-2 border-solid border-white hover:bg-brand-green-light"
            >
              <b>Nilai Diri Saya</b>
            </nuxt-link>
          </div>
        </div>

        <div class="bg-red-400 p-5 mt-4 md:mt-12 md:p-8 rounded-lg">
          <h3 class="text-xl lg:text-2xl text-white">
            <strong>#GotongRoyong Bantu Tenaga Medis</strong>
          </h3>
          <br />
          <div class="flex flex-col lg:flex-row justify-between items-start">
            <div class="text-white w-full lg:w-2/3">
              <p>IDI Cabang Ponorogo Menerima Bantuan Alat Pelindung Diri dan Bahan Kesehatan lain:</p>

              <p class="font-bold my-3">Masker, handsanitizer, sabun dll.</p>

              <p>Yang akan disalurkan ke tenaga dokter yang berjuang melawan Virus Covid19 di fasilitas pelayanan kesehatan di Ponorogo</p>

            </div>
            <i style="flex:0 0 2rem"></i>
            <!-- WA DONASI DESKTOP -->
            <div class="hidden lg:block">
              <btn-wa-donasi></btn-wa-donasi>
            </div>
            <!-- WA DONASI DESKTOP -->
          </div>
          <div class="text-white">
            <div class="lg:text-center my-2">Bantuan dapat diserahkan ke:</div>
            <div class="flex flex-col justify-between lg:flex-row text-base">
              <div class="w-full my-2 lg:my-0 lg:border-r">
                <p>Contact Person</p>
                <p>1. Dr. Riza Mazidu (085655402544) </p>
                <p>2. Dr. Ina kautsar (081335790535)</p>
                <p>3. Dr. Wida Pratiwi (082221228082)</p>
                <p>4. Dr. Iis Kartika (08125975283)</p>
              </div>
              <div class="w-full my-2 lg:my-0 lg:border-r lg:ml-3">
                <p>Kantor IDI PONOROGO</p>
                <p>Perum GRIYA HARMONY BANYUDONO No.A2, </p>
                <p>Jl. Sumatera, Banyudono, Kec. Ponorogo, Kabupaten Ponorogo, Jawa Timur 63411</p>
                <p>Senin - Sabtu </p>
                <p>Jam 08.00 - 12.00</p>
                <p>Menemui Pak Rahmad</p>
              </div>
              <div class="w-full my-2 lg:my-0 lg:ml-3">
                <p>Bisa juga ke</p>
                <p>Rekening Bank BNI Cabang Ponorogo</p>
                <p>0287231600 an Febrina Kautsar</p>
                <p>Dengan nominal transfer 2 digit terakhir angka 11 contoh 100.011 (mohon konfirmasi setelah transfer )</p>
              </div>
            </div>
          </div>
          <!-- WA DONASI MOBILE -->
          <div class="block lg:hidden mt-10 mb-5 lg:my-0">
            <btn-wa-donasi></btn-wa-donasi>
          </div>
          <!-- WA DONASI MOBILE -->
        </div>
      </div>
      <h3 class="font-semibold text-2xl mt-10 mb-5">Peta Persebaran di Ponorogo</h3>
      <div class="list-article">
        <iframe
          style="width:100%;height:400px"
          src="https://fierce-caverns-85065.herokuapp.com/maps"
        ></iframe>
      </div>
       <h3 class="font-semibold text-2xl mt-10 mb-5">Peta Persebaran di Indonesia</h3>
      <div class="list-article">
        <iframe
          style="width:100%;height:470px"
          src="https://fierce-caverns-85065.herokuapp.com/maps-indo"
        ></iframe>
      </div>

      <div class="lg:my-4 text-sm">
        <p class="font-sans">
          *)Note:
          <span
            class="italic"
          >Titik dipeta merupakan titik kordinat desa,bukan merupakan tempat penderita/pasien</span>
        </p>
      </div>

      <h3 class="font-semibold text-2xl mt-10 mb-5">Info Terkini</h3>
      <div class="list-article">
        <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
          <div
            v-for="article in articlesInfoTerkini"
            :key="article.id"
            class="rounded-lg shadow p-6 bg-white mb-3"
          >
            <nuxt-link :to="`/info/${article.id}`" class="font-semibold text-lg hover:underline">
              <h3>{{ article.title.rendered }}</h3>
            </nuxt-link>
            <div v-if="article.excerpt.rendered" v-html="article.excerpt.rendered"></div>
          </div>
        </div>
        <div class="py-5 text-center">
          <nuxt-link
            class="text-blue-400 p-4 rounded border-2 border-blue-300 font-bold text-sm"
            :to="`/category/2`"
          >Lihat Semua Berita</nuxt-link>
        </div>
      </div>

      <h3 class="font-semibold text-2xl mt-10 mb-5">Periksa Fakta</h3>
      <div class="list-article">
        <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
          <div
            v-for="article in articles"
            :key="article.id"
            class="rounded-lg shadow p-6 bg-white mb-3"
          >
            <nuxt-link :to="`/info/${article.id}`" class="font-semibold text-lg hover:underline">
              <h3>{{ article.title.rendered }}</h3>
            </nuxt-link>
            <div v-if="article.excerpt.rendered" v-html="article.excerpt.rendered"></div>
          </div>
        </div>
        <div class="py-5 text-center">
          <nuxt-link
            class="text-blue-400 p-4 rounded border-2 border-blue-300 font-bold text-sm"
            :to="`/category/12`"
          >Lihat Semua Berita</nuxt-link>
        </div>
      </div>

      <h3 class="font-semibold text-2xl mt-10 mb-5">Tips dan Infografik Terbaru</h3>
      <div class="list-article">
        <div class="grid grid-cols-1 lg:grid-cols-2 row-gap-2 col-gap-4">
          <div
            v-for="article in articlesInfoGrafik"
            :key="article.id"
            class="rounded-lg shadow p-6 bg-white mb-3"
          >
            <nuxt-link :to="`/info/${article.id}`" class="font-semibold text-lg hover:underline">
              <h3>{{ article.title.rendered }}</h3>
            </nuxt-link>
          </div>
        </div>
        <div class="py-5 text-center">
          <nuxt-link
            class="text-blue-400 p-4 rounded border-2 border-blue-300 font-bold text-sm"
            :to="`/category/19`"
          >Lihat Semua Berita</nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import BtnWaDonasi from "~/components/BtnWaDonasi";

export default {
  layout: "home",
  components: {
    BtnWaDonasi
  },
  data() {
    return {
      dtIndo: {},
      dtProv: {},
      dtPonorogo: {},
      articles: {},
      articlesInfoTerkini: {},
      articlesInfoGrafik: {}
    };
  },
  created() {
    this.getDtIndo();
    this.getDtProv();
    this.getDtPonorogo();
    this.getArticles();
    this.getArticlesInfoTerkini();
    this.getArticlesInfoGrafik();
  },
  methods: {
    async getDtIndo() {
      const resp = await axios.get("https://api.kawalcorona.com/indonesia/");
      this.dtIndo = resp.data[0];
    },
    async getDtProv() {
      const resp = await axios.get(
        "https://api.kawalcorona.com/indonesia/provinsi/"
      );
      let prov = resp.data.find(pv => pv.attributes.Provinsi == "Jawa Timur");
      this.dtProv = prov;
    },
    async getDtPonorogo() {
      const resp = await axios.get(
        "https://fierce-caverns-85065.herokuapp.com/api/kecamatan"
      );
      this.dtPonorogo = resp.data;
    },
    async getArticles() {
      const resp = await axios.get(
        "https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=12&per_page=4"
      );
      this.articles = resp.data;
    },
    async getArticlesInfoTerkini() {
      const resp = await axios.get(
        "https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=2&per_page=4"
      );
      this.articlesInfoTerkini = resp.data;
    },
    async getArticlesInfoGrafik() {
      const resp = await axios.get(
        "https://kawalcovid19-wp.herokuapp.com/wp/wp-json/wp/v2/posts?categories=19&per_page=4"
      );
      this.articlesInfoGrafik = resp.data;
    }
  }
};
</script>

<style>
.numeric {
  font-family: "Fjalla One";
}
</style>
