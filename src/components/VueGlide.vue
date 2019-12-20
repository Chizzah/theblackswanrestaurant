<template>
  <section>
    <vue-glide class="max-w-6xl mx-auto"
      :perView="1"
      :autoplay="6000"
      :gap="0">
      <vue-glide-slide v-for="(item, i) in items" :key="i">
        <g-image class="md:ml-32 md:h-142 md:rounded" :src="item.images" />
      </vue-glide-slide>
    </vue-glide>
  </section>
</template>

<script>
import { Glide, GlideSlide } from 'vue-glide-js';

export default {
  components: {
    [Glide.name]: Glide,
    [GlideSlide.name]: GlideSlide
  },
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
  }
}
</script>