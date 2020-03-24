<template>
  <div>
    <navigation />
    <div class="bg-gray-100" style="min-height:75vh">
      <nuxt/>
    </div>
  </div>
</template>
<script>
import Navigation from '~/components/Navigation.vue'

export default {
  head: {
    link: [
      { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Fjalla+One' }
    ]
  },
  components: {
    Navigation
  }
}
</script>
