<template>
  <layout>
    <section class="md:text-2xl">
      <section class="relative w-full text-gray-100 bg-gray-900 md:h-128">
        <g-image class="w-full h-full opacity-50 md:opacity-25 md:object-cover" src="../../static/img/chef-preparing-a-meal-in-restaurant-kitchen.webp" alt="" />
        <section class="absolute top-0 left-0 flex flex-col items-center justify-center w-full h-full">
          <h1 class="mx-2 mt-20 text-lg text-center uppercase md:text-4xl">Need a recipe for lamb shanks or a restaurant business plan guide?</h1>
          <h3 class="mx-4 mx-10 my-4 text-center md:text-2xl">Wow your friends & family with our epic recipes or learn what it takes to run your own restaurant.</h3>
        </section>
      </section>
            <section id="latest-articles" class="flex flex-col items-center text-gray-900 justify-items">
        <h2 class="mt-8 text-xl font-bold text-yellow-700 uppercase md:text-2xl md:mt-20">Latest Articles</h2>
        <h3 class="mx-16 font-semibold text-center md:text-2xl md:mb-20">Read our latest blog post about The Black Swan</h3>
        <section class="md:flex md:justify-center md:items-center">
          <ul class="md:flex md:justify-center md:items-center" v-for="edge in $page.blog.edges" :key="edge.node.id">
            <li class="flex flex-col items-center justify-center md:flex-wrap md:mx-40">
              <h3 class="mt-8 font-semibold">{{ edge.node.title }}</h3>
              <h4 class="mb-8 text-sm">by {{ edge.node.author.name }}</h4>
              <g-image width="400" class="md:rounded" :src="edge.node.image.file.url" alt="" />
              <g-link :to="`/post/${edge.node.slug}`"><button class="px-5 py-3 my-8 font-semibold text-gray-100 bg-red-700 shadow-md rounded-xl focus:outline-none">Read More</button></g-link>
            </li>
          </ul>
        </section>
      </section>
    </section>
  </layout>
</template>

<page-query>
query Blog {
  blog: allContentfulPost {
    edges {
      node {
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
  }
}
</page-query>

<script>
export default {

}
</script>

<style>

</style>