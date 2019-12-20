<template>
  <section>
    <vue-glide
      :perView="1"
      :autoplay="6000">
      <vue-glide-slide v-for="(item, i) in items" :key="i">
        <g-image class="md:mx-auto md:h-138" :src="item.images" />
      </vue-glide-slide>
      <template slot="control">
        <button class="px-12 py-3 mt-4 ml-5 font-semibold text-gray-100 uppercase bg-yellow-700 rounded md:text-2xl md:mt-20 md:ml-44" data-glide-dir="<">prev</button>
        <button class="px-12 py-3 mt-4 ml-5 font-semibold text-gray-100 uppercase bg-yellow-700 md:text-2xl md:mt-20 md:ml-110 rounded-xl" data-glide-dir=">">next</button>
      </template>
    </vue-glide>
  </section>
</template>

<script>
import { Glide, GlideSlide } from 'vue-glide-js';

export default {
  data(items) {
    return {
      items: [
        { images: require('../../static/img/black-swan-restaurant-in-lovely-oudtshoorn.webp') },
        { images: require('../../static/img/enjoy-great-food-in-klein-karoo.webp') },
        { images: require('../../static/img/fine-dining-restaurant-in-oudtshoorn.webp') },
        { images: require('../../static/img/the-black-swan-mintt-cafe.webp') },
        { images: require('../../static/img/the-black-swan-premium-wine.webp') },
        { images: require('../../static/img/the-black-swan-shuttle-services.webp') }
      ],
    }
  },
  components: {
    [Glide.name]: Glide,
    [GlideSlide.name]: GlideSlide
  }
}
</script>