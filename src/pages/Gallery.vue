<template>
  <layout>
    <section class="py-8 mt-20 h-96 md:h-96 md:mt-32 md:pb-40 md:h-256">
      <h1 class="mb-8 font-semibold text-center text-yellow-700 uppercase md:text-4xl md:mb-20">Unforgettable memories at <br> The Black Swan Restaurant & Wine Bar <br> in Oudtshoorn, Klein Karoo</h1>
      <VueGlide />
      <p class="my-8 font-semibold text-center uppercase">Swipe</p>
    </section>
  </layout>
</template>

<script>
import VueGlide from '~/components/VueGlide.vue';

export default {
  components: {
    VueGlide
  }
}
</script>