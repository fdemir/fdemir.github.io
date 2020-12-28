<script>
  import Header from './components/layout/Header.svelte'
  import Footer from './components/layout/Footer.svelte'
  import Router from './Router.svelte'
</script>

<style lang="scss" global>
@import './assets/scss/main.scss';
</style>

<main>
  <Header />
  <Router />
  <Footer />
</main>