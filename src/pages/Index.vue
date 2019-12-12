<template>
  <Layout>
    <section id="hero-section" class="relative text-gray-100 bg-gray-900" v-for="edge in $page.hero.edges" :key="edge.node.id">
      <video class="bg-gray-900 opacity-50" muted autoplay loop :src="edge.node.heroVideo.file.url" />
      <section class="absolute top-0 left-0 flex flex-col items-center justify-center w-full h-full">
        <h1 class="mx-8 font-bold text-center uppercase">{{ edge.node.heroTextHeading }}</h1>
        <h3 class="mx-4 my-4 text-sm font-semibold text-center">{{ edge.node.heroTextSubHeading }}</h3>
        <g-link to="/reservetable"><button class="px-4 py-3 text-sm font-semibold text-gray-100 bg-red-700 rounded-lg focus:outline-none">Make A Reservation</button></g-link>
      </section>
    </section>
      <section id="overview-section" class="flex flex-col items-center text-gray-900 bg-gray-100 justify-items">
        <h2 class="mt-8 text-lg font-bold">The Black Swan Restaurant</h2>
        <h3 class="text-sm font-semibold">Fine Dining Restaurant in Oudtshoorn</h3>
        <g-image class="mt-8 mb-4 rounded" src="../../static/img/patrons-of-the-black-swan-restaurant-in-oudtshoon.webp" alt="Patrons enjoying some drinks at The Black Swan Restaurant in Oudtshoorn" />
        <p class="mx-6">Located in the heart of Oudtshoorn, this a lá carte hotspot is a popular restaurant with locals and visitors alike, and is abuzz with activity throughout the year. During the KKNK in March, the Black Swan is ground zero for South Africa’s biggest celebrities who hang out and perform live for the crowds.</p>
        <g-link class="my-8 text-sm text-red-600" to="/about"><p>Find out more About Us...</p></g-link>
      </section>
      <section id="why-us-section" class="py-8 bg-gray-200">
        <h2 class="my-8 text-lg text-center">Why we're unique</h2>
        <section class="flex flex-col items-center justify-center mt-8">
          <section class="flex flex-col items-center justify-center">
            <h3 class="text-sm font-semibold">Wine Bar</h3>
            <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
          </section>
          <section class="mt-8 mb-4">
            <g-image src="../../static/img/the-black-swan-premium-wine.webp" alt="" />
          </section>
          <section class="mt-4">
            <p class="mx-8">Our wine bar is the perfect spot to relax and enjoy an evening out with a loved one or friends. Enjoy the beautiful Klein Karoo while sipping on whites and reds from all around the country, our wine bar lets you unwind in style.</p>
          </section>
        </section>
        <section class="flex flex-col items-center justify-center mt-8">
          <section class="flex flex-col items-center justify-center">
            <h3 class="text-sm font-semibold">Our Menu</h3>
            <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
          </section>
          <section class="mt-8 mb-4">
            <g-image src="../../static/img/the-black-swan-beef-cuisine.webp" alt="" />
          </section>
          <section class="mt-4">
            <p class="mx-8">As the primo fine dining restaurant in Oudtshoorn we wow your tastebuds with mouthwatering dishes and decadent desserts. Come enjoy a traditional ostrich steak and find out why we were voted in the Top 20 Klein Karoo Smulpaap awards.</p>
          </section>
        </section>
        <section class="flex flex-col items-center justify-center mt-8">
          <section class="flex flex-col items-center justify-center">
            <h3 class="text-sm font-semibold">Shuttle Service</h3>
            <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
          </section>
          <section class="mt-8 mb-4">
            <g-image src="../../static/img/the-black-swan-shuttle-services.webp" alt="" />
          </section>
          <section class="mt-4">
            <p class="mx-8">Our shuttle service is free and will take you to and from the restaurant. The result? You can enjoy a glass of wine without worrying about finding your way home afterwards.</p>
          </section>
        </section>
        <section class="flex flex-col items-center justify-center my-8">
          <section class="flex flex-col items-center justify-center">
          <h3 class="text-sm font-semibold">Mintt Street Café & Coffee Shop</h3>
            <div class="w-32 pb-4 border-b border-red-700 border-solid"></div>
          </section>
          <section class="mt-8 mb-4">
            <g-image src="../../static/img/the-black-swan-mintt-cafe.webp" alt="" />
          </section>
          <section class="mt-4">
          <p class="mx-8">Join us at our daytime coffee shop, the Mintt Street Café, for an all-day breakfast and light lunch. Snack on a delicious camembert and fig sandwich, or treat yourself to a traditional ostrich burger alongside freshly hand-cut potato wedges.</p>
          </section>
        </section>
      </section>
      <section id="upcoming-events">
      </section>
      <section id="featured-menu">
        <h2></h2>
      </section>
      <section id="latest-articles" class="flex flex-col items-center text-gray-900 bg-gray-100 justify-items">
        <h2 class="mt-8 text-lg font-bold">Latest Articles</h2>
        <ul v-for="edge in $page.post.edges" :key="edge.node.id">
          <li class="flex flex-col items-center justify-center">
            <h3 class="mt-8 text-sm font-semibold">{{ edge.node.title }}</h3>
            <h4 class="mb-8 text-xs">by {{ edge.node.author.name }}</h4>
            <g-image :src="edge.node.image.file.url" alt="" />
            <g-link :to="edge.node.slug"><button class="px-5 py-3 my-8 font-semibold text-gray-100 bg-red-700 rounded-lg focus:outline-none">Read More</button></g-link>
          </li>
        </ul>
      </section>
      <section id="testimonials-section">
        <h2></h2>
      </section>
      <section id="contact-us" class="flex flex-col items-center justify-center py-8">
        <h2 class="my-4 uppercase">Need to get in touch?</h2>
        <h3 class="mb-8">Head on over to our Contact Page <br> to get all our details</h3>
        <g-link to="/contact" ><button class="px-5 py-3 font-semibold text-gray-100 bg-red-700 rounded-lg focus:outline-none">Contact Us</button></g-link>
      </section>
      <section id="affiliated-section">
        <h2></h2>
      </section>
      <section id="we-accept-section">
        <section>
          <h1></h1>
          <h2></h2>
        </section>
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
    title: 'Hello, world!'
  },
}
</script>