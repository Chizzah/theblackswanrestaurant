<template>
  <layout>
    <section class="md:text-2xl">
      <section class="relative w-full text-gray-100 bg-gray-900 md:h-128">
        <g-image class="w-full h-full opacity-50 md:opacity-25 md:object-cover" src="../../static/img/enjoy-live-music-at-black-swan-restaurant-in-oudtshoorn.webp" alt="Enjoy live entertainment at Black Swan restaurant" />
        <section class="absolute top-0 left-0 flex flex-col items-center justify-center w-full h-full">
          <h1 class="mt-16 mx-2 text-lg text-center uppercase md:text-4xl">Enjoy good music with great food at the Black Swan Restaurant in Oudtshoorn</h1>
          <h3 class="mx-2 my-8 text-center md:text-2xl">Check back regularly to see what events are happening at the Black Swan and the rest of Oudtshoorn</h3>
        </section>
      </section>
      <section id="upcoming-events" class="flex flex-col items-center text-gray-900 justify-items mb-8">
        <h2 class="mt-8 text-xl font-bold text-yellow-700 uppercase md:text-2xl md:mt-20">Upcoming Events</h2>
        <h3 class="mx-8 font-semibold text-center md:text-2xl md:mb-20">Find the latest events happening at the Black Swan Restaurant in Oudtshoorn</h3>
        <section class="flex flex-col justify-center items-center" v-for="edge in $page.events.edges" :key="edge.node.id">
          <g-image class="my-8 md:rounded" :src="edge.node.eventImage.file.url" :alt="edge.node.title" />
          <h4 class="mb-4 mx-4 text-center"><strong>{{ edge.node.title }}</strong></h4>
          <g-link :to="`/event/${edge.node.slug}`"><button class="px-5 py-3 font-semibold text-gray-100 bg-red-700 shadow-md rounded-xl focus:outline-none">Find Out More</button></g-link>
        </section>
      </section>
    </section>
  </layout>
</template>

<page-query>
query Events {
  events: allContentfulEvents {
    edges {
      node {
        id
        slug
        eventImage {
          file {
            url
          }
        }
        title
        description
        date
        time
        location {
          lon
          lat
        }
        admission
      }
    }
  }
}
</page-query>

<script>
export default {

}
</script>