<template>
  <layout>
    <section class="mt-20 md:mt-40 md:flex md:justify-start md:items-start">
      <AuthorCard />
      <section class="m-8">
        <h2 class="mb-4 md:text-lg">{{ $page.post.date }}</h2>
        <h1 class="mb-8 text-3xl md:text-6xl">{{ $page.post.title }}</h1>
        <p class="mb-8 md:mr-20 md:text-2xl"><span class="font-extrabold text-red-700 uppercase">Quick Summary:</span> {{ $page.post.summary }}</p>
        <section class="flex items-center justify-center md:mr-20 md:my-20">
          <g-image :src="$page.post.image.file.url" :alt="$page.post.title" />
        </section>
        <div class="mx-6 my-8 md:mr-20 md:text-2xl" v-html="$page.post.body" />
      </section>
    </section>
  </layout>
</template>

<page-query>
query Post($path: String!) {
  post: contentfulPost(path: $path) {
    id
    slug
    date(format: "MMMM DD, YYYY")
    title
    author {
      name
      authorImage {
        file {
          url
        }
      }
      facebook
    }
    seo {
      title
      description
    }
    summary
    body(html:true)
    image {
      file {
        url
      }
    }
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