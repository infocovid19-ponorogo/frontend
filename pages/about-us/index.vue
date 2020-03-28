<template>
  <div class="w-full mt-5">
    <div class="container mx-auto px-5 ">
      <h1 class="text-3xl font-bold">Tentang Kami</h1>
      <p class="my-3">Pada Selasa siang  tanggal 24 Maret 2020,Pemerintah Kabupaten Ponorogo merilis data terkait sebaran Covid19 di Ponorogo, kami pegiat teknologi dan data yang diisi oleh anak-anak muda Ponorogo merasa perlu untuk memberikan informasi yang akurat dan terpercaya terkait Covid19 di Ponorogo. Inisiatif ini diluncurkan karena keprihatinan akan kesimpangsiuran informasi yang beredar di Ponorogo mengenai COVID-19.</p>
      <p class="my-3">Website               <a href="https://infocovid19ponorogo.id" style="color:blue">infocovid19ponorogo.id</a>
 beserta akun-akun media sosialnya               <a href="https://instagram.com/infocovid19ponorogo" style="color:blue">@infocovid19ponorogo</a>
 di Instagram akan dimutakhirkan berkala dengan esensi isi:</p>
      <h3 class="text-xl font-bold">1/ Informasi</h3>
      <p class="my-3">Kurasi dan analisis atas informasi yang beredar (news explainer / newsplainer), dengan mengedepankan hanya poin-poin yang berdasarkan bukti dan fakta, bukan hipotesis, opini atau dugaan.</p>
      <h3 class="text-xl font-bold">2/ Verifikasi</h3>
      <p class="my-3">Membantah kabar burung, mengklarifikasi informasi yang simpang siur dan memberikan penjelasan yang lugas. </p>
      <h3 class="text-xl font-bold">3/ Edukasi</h3>
      <p class="my-3">Menyampaikan ke publik hal-hal yang perlu dan bisa dilakukan, hal-hal yang perlu dihindari, serta tips-tips kesehatan lain yang mudah diaplikasikan oleh setiap orang dan kelompok masyarakat, seperti di sekolah, tempat kerja, rumah makan dan tempat-tempat umum.</p>
      <div class="ml-5">
        <p class="my-3">Tim relawan membagi dirinya dalam tiga tim:</p>
        <p class="my-3">-Tim teknologi – yang menyiapkan infrastruktur teknologi. Tim ini dipimpin oleh <a href="https://github.com/zainras" style="color:blue">Zain</a> dan <a href="https://github.com/iamwahid" style="color:blue">Niam Wahid</a> dengan didukung dengan data akurat dari Pemerintah Kabupaten Ponorogo.</p>
        <p class="my-3">-Tim data – yang memonitor perkembangan isu dengan mengumpulkan informasi yang beredar, mengecek akurasinya serta menganalisa.</p>
        <p class="my-3">-Tim konten – yang membuat tulisan beserta visualnya untuk dipublikasikan.</p>
      </div>
      <p class="my-3">Untuk informasi lebih lanjut dapat menghubungi:</p>
      <div class="table w-full border mt-5">
        <div class="table-row-group border">
          <div class="table-row border">
            <div class="table-cell text-gray-700 px-4 py-2 border border-gray-200">Instagram</div>
            <div class="table-cell text-gray-700 px-4 py-2 border border-gray-200">
              <a href="https://instagram.com/infocovid19ponorogo" style="color:blue">@infocovid19ponorogo</a>
            </div>
          </div>
          <div class="table-row border">
            <div class="table-cell text-gray-700 px-4 py-2 border border-gray-200">Situs</div>
            <div class="table-cell text-gray-700 px-4 py-2 border border-gray-200">
              <a href="https://infocovid19ponorogo.id" style="color:blue">infocovid19ponorogo.id</a>
            </div>
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
    return { dtIndo }
  }
}
</script>

<style>

</style>
