<template>
<div>
    <footer class="text-gray-500 bg-black sm:rounded-xl">
      <section class="border-b border-gray-600 border-solid md:ml-24">
        <h4 class="pt-16 mx-8 mb-4 text-xs font-semibold text-red-700 uppercase">Fine dining at its best</h4>
        <h1 class="mx-8 mb-6 text-gray-100 text-md">Join us at the best fine dining restaurant in Oudtshoorn & the Klein Karoo.</h1>
        <h3 class="mx-8 mr-6 text-sm">Experience an evening you'll never forget at the Black Swan Restaurant & Wine Bar. Bring a loved one or a few friends and let us be a part of your wonderful memories.</h3>
        <g-link to="/reservetable"><button class="px-6 py-3 mx-8 my-12 font-semibold text-gray-100 bg-red-700 rounded-xl focus:outline-none">Make A Reservation</button></g-link>
      </section>
      <section class="flex flex-row items-start justify-around mb-8 text-sm flex-nowrap">
          <section class="my-8">
            <h2 class="text-gray-100">Navigation</h2>
            <ul class="text-gray-500 rounded list-reset" v-for="navItem in navItems" :key="navItem.title">
              <li class="my-3">
                <g-link :to="`${navItem.route}`">{{ navItem.title }}</g-link>
              </li>
            </ul>
          </section>
          <section class="mt-8">
            <h2 class="text-gray-100">Our Menu</h2>
            <ul class="text-gray-500 rounded list-reset" v-for="menuItem in menuItems" :key="menuItem.title">
              <li class="my-3">
                <g-link :to="`${menuItem.route}`">{{ menuItem.title }}</g-link>
              </li>
            </ul>
          </section>
        <section class="mt-8">
          <h2 class="text-gray-100">Get in touch</h2>
          <ul class="text-gray-500 rounded list-reset" v-for="contactItem in contactItems" :key="contactItem.title">
            <li class="my-3">
              <g-link :to="`${contactItem.route}`">{{ contactItem.title }}</g-link>
            </li>
          </ul>
        </section>
      </section>
    </footer>
        <div class="py-2 mx-4 text-xs text-center border-solid sm:order-2">
            <p class="mb-4">JAMstack Website by <span class="font-semibold hover:text-green-400">Chadd Web Design</span></p>
            <p class="mb-2">Copyright &copy; {{ new Date().getFullYear() }} The Black Swan Restaurant & Wine Bar. All rights reserved.</p>
        </div>
      </div>
</template>

<script>
export default {
  data() {
    return {
      navItems: [
        { title:'Home', route:'/' },
        { title:'About', route:'/about' },
        { title:'Events', route:'/events' },
        { title:'Gallery', route:'/gallery' },
        { title:'Blog', route:'/blog' },
        { title:'Privacy', route:'/privacy' },
        { title:'Cookies', route:'/cookies' }
      ],
      menuItems: [
        { title:'Starters', route:'/starters' },
        { title:'Mains', route:'/mains' },
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