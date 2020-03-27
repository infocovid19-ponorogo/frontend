<template>
  <a
    :href="linkDonasi"
    target="_blank"
    class="px-10 py-4 rounded-lg text-white border-2 border-solid border-white hover:bg-brand-green-light"
  >
    <b>Donasi Sekarang</b>
  </a>
</template>

<script>
export default {
  data() {
    return {
      nomorTujuan: '6281335790535',
      textPesan: 'Assalamuaalikum%20Warohamtullah%20Wabarokatuh.%0D%0A%0D%0A'
                  + 'Saya ingin berdonasi membantu tenaga dokter yang berjuang melawan Virus Covid19 di fasilitas pelayanan kesehatan di Ponorogo.'
    }
  },
  computed: {
    linkDonasi() {
      return `https://web.whatsapp.com/send?phone=${this.nomorTujuan}&text=${this.textPesan}`
    }
  }
};
</script>
<style>
</style>
