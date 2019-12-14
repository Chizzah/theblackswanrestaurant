<template>
  <section>
    <div class="flex items-center justify-center mt-8">
      <div class="border-b-2 border-red-700 border-solid w-92"></div>
    </div>
    <section class="m-8">
      <g-image class="border-4 border-red-700 border-solid rounded-full" :src="$page.post.author.authorImage.file.url" alt="" />
    </section>
    <section class="m-8">
      <h4 class="font-semibold text-gray-800 uppercase">About The Author</h4>
      <p class="mt-4">{{ $page.post.author.name }} lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid animi, omnis sint distinctio incidunt nemo ducimus vel eligendi vero sunt enim modi cum similique ea rerum aperiam eveniet sed velit.</p>
    </section>
    <section class="flex items-center justify-start m-8">
      <g-image src="../../static/icons/author-facebook.svg" alt="Link to Ryan Dammert's Facebook Page on The Black Swan Restaurant website blog post." width="15" /><a class="ml-4 text-blue-500 underline uppercase" :href="$page.post.author.facebook">Facebook</a>
    </section>
    <div class="flex items-center justify-center">
      <div class="border-b-2 border-red-700 border-solid w-92"></div>
    </div>
  </section>
</template>