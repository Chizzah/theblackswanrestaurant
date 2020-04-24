<template>
  <layout>
    <section class="md:text-2xl">
      <section class="relative w-full text-gray-100 bg-gray-900 md:h-128">
        <g-image class="w-full h-full opacity-50 md:opacity-25 md:object-cover" src="../../static/img/enjoy-great-food-in-klein-karoo.webp" alt="The best food in Oudtshoorn" />
        <section class="absolute top-0 left-0 flex flex-col items-center justify-center w-full h-full">
          <h1 class="mt-16 text-lg text-center uppercase md:text-4xl">The most memorable <br> culinary experience in the Klein Karoo</h1>
          <h3 class="mx-4 mx-10 my-8 text-center md:text-2xl">We'd love to be a part of your journey</h3>
        </section>
      </section>
      <section class="mt-6 mb-20 md:mt-12">
        <Tabs />
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

<script>
import Tabs from '~/components/Tabs';

export default {
  components: {
    Tabs
  }
}
</script>