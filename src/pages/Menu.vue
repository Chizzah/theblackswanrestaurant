<template>
  <layout>
    <section class="md:text-2xl">
      <section class="relative w-full text-gray-100 bg-gray-900 md:h-128">
        <g-image class="w-full h-full opacity-50 md:opacity-25 md:object-cover" src="../../static/img/enjoy-great-food-in-klein-karoo.webp" alt="" />
        <section class="absolute top-0 left-0 flex flex-col items-center justify-center w-full h-full">
          <h1 class="mt-16 text-lg text-center uppercase md:text-4xl">The most memorable <br> culinary experience in the Klein Karoo</h1>
          <h3 class="mx-4 mx-10 my-8 text-center md:text-2xl">We'd love to be a part of your journey</h3>
        </section>
      </section>
      <section class="mb-20">
        <section>
          <h2 class="mt-16 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:text-2xl">Appetisers</h2>
          <section v-for="edge in $page.appetisers.edges" :key="edge.node.id">
            <section class="flex items-center justify-between">
              <h3 class="my-4 ml-4 font-semibold">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-extrabold text-yellow-700">{{ edge.node.price }}</h4>
            </section>
            <section class="flex items-center justify-center">
              <g-image src="../../static/img/black-swan-restaurant-in-lovely-oudtshoorn.webp" alt="" width="50" />
              <h5 class="ml-4 w-88">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
        <section>
          <h2 class="mt-16 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:text-2xl">Mains</h2>
          <section v-for="edge in $page.mains.edges" :key="edge.node.id">
            <section class="flex items-center justify-between">
              <h3 class="my-4 ml-4 font-semibold">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-extrabold text-yellow-700">{{ edge.node.price }}</h4>
            </section>
            <section class="flex items-center justify-center">
              <g-image src="../../static/img/black-swan-restaurant-in-lovely-oudtshoorn.webp" alt="" width="50" />
              <h5 class="ml-4 w-88">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
        <section>
          <h2 class="mt-16 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:text-2xl">Specialities</h2>
          <section v-for="edge in $page.specialities.edges" :key="edge.node.id">
            <section class="flex items-center justify-between">
              <h3 class="my-4 ml-4 font-semibold">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-extrabold text-yellow-700">SQ</h4>
            </section>
            <section class="flex items-center justify-center">
              <g-image src="../../static/img/black-swan-restaurant-in-lovely-oudtshoorn.webp" alt="" width="50" />
              <h5 class="ml-4 w-88">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
        <section>
          <h2 class="mt-16 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:text-2xl">Desserts</h2>
          <section v-for="edge in $page.desserts.edges" :key="edge.node.id">
            <section class="flex items-center justify-between">
              <h3 class="my-4 ml-4 font-semibold">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-extrabold text-yellow-700">{{ edge.node.price }}</h4>
            </section>
            <section class="flex items-center justify-center">
              <g-image src="../../static/img/black-swan-restaurant-in-lovely-oudtshoorn.webp" alt="" width="50" />
              <h5 class="ml-4 w-88">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
      </section>
    </section>
  </layout>
</template>

<page-query>
  query Menu {
    appetisers: allContentfulAppetisers {
      edges {
        node {
          id
          name
          description
          price
        }
      }
    }
    mains: allContentfulMains {
      edges {
        node {
          id
          name
          description
          price
          category
        }
      }
    }
    specialities: allContentfulSpecialities {
      edges {
        node {
          id
          name
          description
        }
      }
    }
    desserts: allContentfulDesserts {
      edges {
        node {
          id
          name
          description
          price
        }
      }
    }
  }
</page-query>