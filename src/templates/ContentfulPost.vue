<template>
  <layout>
    <AuthorCard />
    <section class="m-8">
      <h2 class="mb-4">{{ $page.post.date }}</h2>
      <h1 class="mb-8 text-3xl md:text-6xl">{{ $page.post.title }}</h1>
      <p class="mb-8"><span class="font-extrabold text-red-700 uppercase">Quick Summary:</span> {{ $page.post.summary }}</p>
      <g-image :src="$page.post.image.file.url"/>
      <div class="mx-6 my-8" v-html="$page.post.body" />
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