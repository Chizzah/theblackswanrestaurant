<template>
  <Layout>
    <section class="max-w-lg mx-auto mt-20 md:mt-40 md:max-w-6xl">
      <h2 class="text-xl font-bold text-center text-yellow-700 md:text-3xl md:mx-32 md:mb-20">Amazing food & unforgettable memories at The Black Swan Restaurant & Wine Bar in Oudtshoorn, Klein Karoo</h2>
      <Carousel />
    </section>
  </Layout>
</template>

<script>
import Carousel from '~/components/Carousel';

export default {
  metaInfo: {
    title: "Gallery"
  },
  components: {
    Carousel
  },
}
</script>