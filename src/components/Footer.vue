<template>
  <footer class="text-gray-500 bg-black md:rounded-xl md:mb-16 md:max-w-6xl md:mx-auto">
    <section class="mt-8 border-b border-gray-600 border-solid md:ml-24 md:mt-16">
      <h4 class="pt-16 mx-8 mb-4 text-xs font-semibold text-red-700 uppercase md:text-lg">Fine dining at its best</h4>
      <h2 class="mx-8 mb-6 text-gray-100 text-md md:text-3xl">Join us at the best fine dining restaurant <br class="hidden md:block"> in Oudtshoorn & the Klein Karoo.</h2>
      <h3 class="mx-8 mr-6 text-sm md:text-xl">Experience an evening you'll never forget at the Black Swan<br class="hidden md:block"> Restaurant & Wine Bar. Bring a loved one or a few friends and<br class="hidden md:block"> let us be a part of your wonderful memories.</h3>
      <g-link to="/reservetable"><button class="px-6 py-3 mx-8 my-12 font-semibold text-gray-100 bg-red-700 rounded-xl focus:outline-none md:text-lg">Make A Reservation</button></g-link>
    </section>
    <section class="flex flex-row items-start justify-around mb-8 text-sm text-left md:justify-end md:w-full md:text-lg">
      <section class="my-8 ml-1 md:mr-20">
        <h3 class="text-gray-100">Navigation</h3>
        <ul class="text-gray-500 rounded list-reset" v-for="navItem in navItems" :key="navItem.title">
          <li class="my-3">
            <g-link :to="`${navItem.route}`">{{ navItem.title }}</g-link>
          </li>
        </ul>
      </section>
      <section class="mt-8 md:mr-16">
        <h3 class="text-gray-100">Menu</h3>
        <ul class="text-gray-500 rounded list-reset" v-for="menuItem in menuItems" :key="menuItem.title">
          <li class="my-3">
            <g-link :to="`${menuItem.route}`">{{ menuItem.title }}</g-link>
          </li>
        </ul>
      </section>
      <section class="mt-8 mr-2 md:mr-16">
        <h3 class="text-gray-100">Get in touch</h3>
        <ul class="text-gray-500 rounded list-reset" v-for="contactItem in contactItems" :key="contactItem.title">
          <li class="my-3">
            <g-link :to="`${contactItem.route}`">{{ contactItem.title }}</g-link>
          </li>
        </ul>
      </section>
    </section>
    <section class="py-2 mx-4 text-xs text-center border-solid md:order-2">
      <p class="mb-4 md:ml-16">JAMstack Website by <a href="http://chaddwebdesign.co.za" target="_blank"><span class="font-semibold hover:text-green-400">Chadd Web Design</span></a></p>
      <p class="mb-2 md:ml-8 md:mb-8">Copyright &copy; {{ new Date().getFullYear() }} The Black Swan Restaurant & Wine Bar. All rights reserved.</p>
    </section>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      navItems: [
        { title:'Home', route:'/' },
        { title:'About', route:'/about' },
        { title:'Events', route:'/events' },
        { title:'Blog', route:'/blog' },
        { title:'Gallery', route:'/gallery' },
        { title:'Privacy', route:'/privacypolicy' },
      ],
      menuItems: [
        { title:'Appetisers', route:'/appetisers' },
        { title:'Mains', route:'/mains' },
        { title:'Specialities', route:'/specialities' },
        { title:'Desserts', route:'/desserts' },
        { title:'Wine List', route:'/winelist' },
      ],
      contactItems: [
        { title:'Make Reservation', route:'/reservetable' },
        { title:'Contact Us', route:'/contact' },
      ],
      isOpen: false,
    }
  }
}
</script>