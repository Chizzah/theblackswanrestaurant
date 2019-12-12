<template>
  <main class="max-w-6xl mx-auto">
    <Nav />
    <slot />
    <Footer />
  </main>
</template>

<script>
import Nav from '~/components/Nav.vue';
import Footer from '~/components/Footer.vue';

export default {
  components: {
    Nav,
    Footer
  }  
}
</script>

<style lang="postcss">
  html {
    scroll-behaviour: smooth;
    font-family: 'Open Sans', sans-serif;
  }

  body {
    background: #F7FAFC;
  }

  h1,
  h2 {
    font-family: 'Amaranth', sans-serif;
  }
</style>