<template>
  <layout>
    <section class="mt-20 md:mt-40 flex flex-col justify-center items-center md:text-2xl">
      <h1 class="text-lg text-center uppercase text-yellow-700 md:text-4xl">{{ $page.events.title }}</h1>
      <g-image class="my-8 md:my-16 md:rounded" :src="$page.events.eventImage.file.url" />
      <p class="mb-4 text-center">{{ $page.events.description }}</p>
      <p class="mb-4 text-center"><strong>Date:</strong> {{ $page.events.date }}</p>
      <p class="mb-4 text-center"><strong>Time:</strong> {{ $page.events.time }}</p>
      <p class="mb-4 text-center"><strong>Admission:</strong> R{{ $page.events.admission }}</p>      
    </section>
  </layout>
</template>

<page-query>
  query Events($path: String!) {
    events: contentfulEvents(path: $path) {
      id
      slug
      eventImage {
        file {
          url
        }
      }
      title
      description
      date(format: "MMMM DD, YYYY")
      time
      admission
    }
  }
</page-query>

<script>
import AuthorCard from '~/components/AuthorCard';

export default {
  components: {
    AuthorCard
  }
}
</script>