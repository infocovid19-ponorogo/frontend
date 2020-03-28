<template>
  <div class="w-full mt-5">
    <div class="container mx-auto px-5 ">
      <h1 class="text-3xl font-bold">Kebijakan Privasi</h1>
     <br>
     <br>
     <p><a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> adalah upaya kerja sama netizen pro data dan independen untuk memberikan edukasi dan verifikasi, serta menyampaikan informasi terkini terkait COVID-19. Data dan informasi yang ditampilkan di sini merupakan agregasi dari berbagai data yang diambil dari sumber-sumber pemerintah, LSM kesehatan dan media yang telah diterbitkan. Semua data dan gambar yg ditampilkan di situs ini akan memuat sumber yang digunakan sebagai referensi. <a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> berupaya dengan sebaik mungkin untuk memastikan bahwa data yang ditampilkan telah diverifikasi dan adalah yang sebenar-benarnya. <strong>Apabila ada informasi dan/atau data yang tidak akurat ataupun tidak benar, <a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> akan menarik informasi dan/atau data tersebut, dan bilamana memungkinkan, memberikan masukan atas ketidakakuratan data dan/atau informasi tersebut kepada sumber data.</strong></p>
     <br>
     <br>
     <p><a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> tidak menerima imbalan apa pun dari pihak mana pun, dan tidak akan menjual data yang didapat dan tersedia di laman ini kepada pihak mana pun. <strong>Semua data yang tersedia di <a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> boleh disebarluaskan dengan menyertakan pranala sumber lama <a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> tanpa melakukan perubahan, penambahan atau pun pengurangan dari hal yang termuat di laman yang dikutip. <a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> tidak bertanggung jawab apabila ada pihak luar yang mengambil data dari <a href="https://infocovid19ponorogo.id/">Infocovid19ponorogo</a> untuk kemudian direkayasa demi kepentingan pribadi mereka</strong>.</p>

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
