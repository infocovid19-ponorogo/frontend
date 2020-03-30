<template>
  <div class="w-full mt-5">
    <div class="container mx-auto px-5">
      <div id="article-content">
        <h1 class="text-3xl font-bold">Pernyataan Resmi</h1>
        <p>Menyikapi adanya beberapa masukan terkait visualisasi data dalam bentuk peta untuk tidak ditampilkan dan juga adanya kesalahan teknis dari sisi programming kami. Kami dari infocovid19ponorogo.id mengambil langkah untuk tidak menampilkan peta persebaran yang ada.</p>

        <p>Senin, 30 Maret 2020, kami mendatangi Kominfo Ponorogo terkait penyesuaian data dan juga permintaan maaf terkait kesalahan penyajian data. Dari pihak Kominfo Ponorogo telah memberikan saran agar lebih berhati-hati sekaligus pernyataan agar data yang disajikan benar-benar valid dan mengikuti data yang bersumber di website <a href="https://ponorogo.go.id/corona">https://ponorogo.go.id/corona</a>.</p>

        <p>Jika diluar sana ada yang memberitakan bahwa kami menyebarkan hoax itu sungguh sangat keliru, karena tidak ada hal yang kami sengaja di dalam kekeliruan kami. Tentu kami bisa mengajukan keberatan atas berita yang beredar tentang tuduhan itu,tetapi kami percaya <strong>kebermanfaatan website ini jauh lebih banyak ketimbang isu negatifnya.</strong></p>

        <p>Sebenarnya dalam website kami sudah ada kebijakan privasi terkait konten yang ada,bisa dibaca pada <a href="https://infocovid19ponorogo.id/policy-privacy/">https://infocovid19ponorogo.id/policy-privacy/</a>  dan website ini juga merujuk pada lisensi internasional <a href="https://creativecommons.org/licenses/by-nc-nd/4.0/legalcode.id">https://creativecommons.org/licenses/by-nc-nd/4.0/legalcode.id</a>.Jika ada kekeliruan atau kesalahan data yang kami tampilkan bisa dikoreksi dan kami akan meralat sebagai bentuk pertanggung jawaban kami.</p>

        <p>Dengan berat hati kami menutup akses peta persebaran di website kami,terima kasih atas perhatian pengunjung dan pembaca yang telah mengakses website kami.</p>

        <p>Kami akan terus berusaha untuk tidak berhenti menginfokan sesuatu yang bermanfaat kepada masyarakat khususnya Masyarakat Ponorogo.Sekali lagi terima kasih atas support kritik dan sarannya.</p>

        <p>Demikian klarifikasi dari kami,terima kasih.</p>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  layout: "home",
  async asyncData({ $axios }) {
    const dtIndo = await $axios.$get(
      "https://kawalcovid19.harippe.id/api/summary"
    );
    return { dtIndo };
  }
};
</script>

<style>
#article-content {
  overflow-wrap: break-word;
}
#article-content h1 {
  margin-bottom: 18px;
  font-size: 36px;
  line-height: 36px;
  font-weight: 600;
}
#article-content h2 {
  margin-bottom: 16px;
  font-size: 32px;
  line-height: 36px;
  font-weight: 600;
}
#article-content h3 {
  margin-bottom: 14px;
  font-size: 28px;
  line-height: 36px;
  font-weight: 600;
}
#article-content h4 {
  margin-bottom: 12px;
  font-size: 24px;
  line-height: 36px;
  font-weight: 600;
}
#article-content h5 {
  margin-bottom: 10px;
  font-size: 20px;
  line-height: 36px;
  font-weight: 600;
}
#article-content h6 {
  margin-bottom: 8px;
  font-size: 14px;
  line-height: 36px;
  font-weight: 600;
}
#article-content p {
  line-height: 24px;
  margin-bottom: 16px;
}
#article-content ul {
  display: block;
  list-style-type: none;
  margin: 12px 12px 16px 16px;
  padding: 0px;
}
#article-content ul li {
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
#article-content a {
  color: #63b3ed;
}
</style>
