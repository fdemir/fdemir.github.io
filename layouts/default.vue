<template>
  <div id="wrapper">
    <Header />
    <Nuxt />
    <!-- <SocialMedia /> -->
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header'
export default {
  components: {
    Header,
  },
}
</script>
