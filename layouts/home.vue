<template>
  <div>
    <navigation />
    <div class="bg-gray-100 py-24 lg:py-32" style="min-height:75vh">
      <nuxt/>
    </div>
    <app-footer />
  </div>
</template>
<script>
import Navigation from '~/components/Navigation.vue'
import AppFooter from '~/components/AppFooter.vue'

export default {
  head: {
    link: [
      { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Fjalla+One' }
    ]
  },
  components: {
    Navigation,
    AppFooter,
  }
}
</script>
