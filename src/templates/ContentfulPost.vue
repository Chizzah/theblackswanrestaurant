<template>
  <layout>
    <section v-if="edge in $page.post.edges" :key="edge.node.id">
      <h1>{{ edge.node.title }}</h1>
      <h2>{{ edge.node.author.name }}</h2>
      <g-image :src="edge.node.image.file.url" />
    </section>
  </layout>
</template>

<page-query>
query Post($path: String!) {
  post: contentfulPost(path: $path) {
    id
    title
    slug
    author {
      name
      facebook
    }
    image {
      file {
        url
      }
    }
  }
}
</page-query>