<template>
  <Layout>
    <section class="text-gray-900 bg-gray-100 md:text-2xl">
      <section id="hero-section" class="relative text-gray-100 bg-gray-900 md:h-screen" v-for="edge in $page.hero.edges" :key="edge.node.id">
        <video class="w-full h-full bg-gray-900 opacity-50 md:opacity-25 md:object-cover" muted autoplay loop :src="edge.node.heroVideo.file.url" />
        <section class="absolute top-0 left-0 flex flex-col items-center justify-start w-full h-full mt-24 md:justify-start md:mt-56">
          <h1 class="mx-12 font-semibold text-center uppercase md:text-4xl md:mx-128 md:mb-20">{{ edge.node.heroTextHeading }}</h1>
          <h3 class="hidden mx-4 my-4 font-semibold text-center md:block md:text-2xl md:mx-110 md:mb-20">{{ edge.node.heroTextSubHeading }}</h3>
          <g-link to="/reservetable"><button class="hidden px-4 py-3 mb-2 text-sm font-semibold text-gray-100 bg-red-700 shadow-md md:block rounded-xl focus:outline-none md:text-2xl">Make A Reservation</button></g-link>
        </section>
        <section class="flex flex-col items-center justify-center h-56 text-gray-900 bg-gray-100 sm:hidden">
          <h3 class="mx-4 my-4 font-semibold text-center md:block md:text-2xl md:mx-96 md:mb-20">{{ edge.node.heroTextSubHeading }}</h3>
          <g-link to="/reservetable"><button class="px-4 py-3 mb-2 text-sm font-semibold text-gray-100 bg-red-700 shadow-md rounded-xl focus:outline-none md:text-2xl">Make A Reservation</button></g-link>
        </section>
      </section> 
      <section id="overview-section" class="flex flex-col items-center text-gray-900 bg-gray-200 justify-items md:h-screen">
        <h2 class="mx-8 mt-8 text-xl font-bold text-yellow-700 md:text-3xl md:mt-20">The Black Swan Restaurant</h2>
        <h3 class="font-semibold text-center md:text-2xl">Fine Dining Restaurant in Oudtshoorn</h3>
        <section class="md:flex md:items-center md:justify-around md:py-20">
          <section class="md:ml-8 md:md:w-2/3">
            <g-image class="mt-8 mb-4 md:rounded md:mt-0" width="650" height="400" src="../../static/img/patrons-of-the-black-swan-restaurant-in-oudtshoon.webp" alt="Patrons enjoying some drinks at The Black Swan Restaurant in Oudtshoorn" />
          </section>
          <section class="md:w-1/2">
            <p class="mx-6 md:mx-20">Located in the heart of Oudtshoorn, this a lá carte hotspot is a popular restaurant with locals and visitors alike, and is abuzz with activity throughout the year. During the KKNK in March, the Black Swan is ground zero for South Africa’s biggest celebrities who hang out and perform live for the crowds.</p>
            <g-link to="/about"><h4 class="my-8 text-sm font-semibold text-center text-red-600 uppercase md:text-left md:ml-20">Find out more About Us...</h4></g-link>
          </section>
        </section>
      </section><section id="why-us-section" class="flex flex-col items-center justify-center max-w-5xl py-16 mx-auto">
        <h2 class="mt-8 text-xl font-bold text-center text-yellow-700 md:text-3xl">Why we're unique</h2>
        <h3 class="mb-8 font-semibold text-center md:mb-16 md:text-2xl">Find delight in the Klein Karoo</h3>
        <section class="items-center justify-center text-sm md:flex">
          <section class="flex flex-col items-center justify-center md:w-1/2">
            <h3 class="font-semibold">Wine Bar</h3>
            <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
            <g-image class="mt-8 md:rounded" width="350" height="200" src="../../static/img/the-black-swan-premium-wine.webp" alt="" />
            <p class="m-8 md:w-1/2">Our wine bar is the perfect spot to relax and enjoy an evening out with a loved one or friends. Enjoy the beautiful Klein Karoo while sipping on whites and reds from all around the country, our wine bar lets you unwind in style.</p>
          </section>
          <section class="flex flex-col items-center justify-center md:w-1/2">
            <h3 class="font-semibold">Our Menu</h3>
            <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
            <g-image class="mt-8 md:rounded" width="350" height="200" src="../../static/img/the-black-swan-beef-cuisine.webp" alt="" />
            <p class="m-8 md:w-1/2">As the primo fine dining restaurant in Oudtshoorn we wow your tastebuds with mouthwatering dishes and decadent desserts. Come enjoy a traditional ostrich steak and find out why we were voted in the Top 20 Klein Karoo Smulpaap awards.</p>
          </section>
        </section>
          <section class="items-center justify-center my-4 text-sm md:flex">
            <section class="flex flex-col items-center justify-center md:w-1/2">
              <h3 class="font-semibold">Shuttle Service</h3>
              <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
              <g-image class="mt-8 md:rounded" width="350" height="200" src="../../static/img/the-black-swan-shuttle-services.webp" alt="" />
              <p class="m-8 md:w-1/2">Our shuttle service is free and will take you to and from the restaurant. The result? You can enjoy a glass of wine without worrying about finding your way home afterwards.</p>
            </section>
            <section class="flex flex-col items-center justify-center md:w-1/2">
              <h3 class="mt-10 font-semibold">Mintt Street Café</h3>
              <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
              <g-image class="mt-8 md:rounded" width="350" height="200" src="../../static/img/the-black-swan-mintt-cafe.webp" alt="" />
              <p class="m-8 md:w-1/2">Join us at our daytime coffee shop, the Mintt Street Café, for an all-day breakfast and light lunch. Snack on a delicious camembert and fig sandwich, or treat yourself to a traditional ostrich burger alongside freshly hand-cut potato wedges.</p>
            </section>
          </section>
        </section>
      </section>
      <section id="latest-articles" class="flex flex-col items-center text-gray-900 bg-gray-200 justify-items">
        <h2 class="mt-8 text-xl font-bold text-yellow-700 uppercase md:text-2xl md:mt-20">Latest Articles</h2>
        <h3 class="mx-16 font-semibold text-center md:text-2xl md:mb-20">Read our latest blog post about The Black Swan</h3>
        <section class="md:flex md:justify-center md:items-center">
          <ul class="md:flex md:justify-center md:items-center" v-for="edge in $page.post.edges" :key="edge.node.id">
            <li class="flex flex-col items-center justify-center md:flex-wrap md:mx-40">
              <h3 class="mt-8 font-semibold">{{ edge.node.title }}</h3>
              <h4 class="mb-8 text-sm">by {{ edge.node.author.name }}</h4>
              <g-image width="400" class="md:rounded" :src="edge.node.image.file.url" alt="" />
              <g-link :to="`/post/${edge.node.slug}`"><button class="px-5 py-3 my-8 font-semibold text-gray-100 bg-red-700 shadow-md rounded-xl focus:outline-none">Read More</button></g-link>
            </li>
          </ul>
        </section>
      </section>
      <section id="upcoming-events">
      </section>
      <section id="featured-menu">
        <h2></h2>
      </section>
      <section id="testimonials-section">
        <h2></h2>
      </section>
      <section id="contact-us" class="flex flex-col items-center justify-center py-8 text-center bg-gray-100">
        <h2 class="mx-8 my-4 text-xl font-bold text-yellow-700 uppercase md:text-2xl">Need to get in touch?</h2>
        <h3 class="mx-4 mb-8 md:text-2xl">Head on over to our Contact Page to get all our details</h3>
        <g-link to="/contact" ><button class="px-5 py-3 font-semibold text-gray-100 bg-red-700 shadow-md rounded-xl focus:outline-none">Contact Us</button></g-link>
      </section>
      <section id="affiliated-section">
        <h2></h2>
      </section>
      <section id="we-accept-section">
      </section>
      <section>
      
    </section>
  </Layout>
</template>

<page-query>
query Post {
  post: allContentfulPost {
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
  hero: allContentfulHeroSection {
    edges {
      node {
        id
        title
        heroVideo {
          file {
            url
          }
        }
        heroTextHeading
        heroTextSubHeading
      }
    }
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: 'Fine Dining Restaurant in Oudtshoorn | The Black Swan'
  },
  meta: [
    {
      name: 'description',
      content: 'Located in the heart of Oudtshoorn, this hotspot is a popular restaurant with locals and visitors alike, and is abuzz with activity throughout the year.'
    }
  ]
}
</script>