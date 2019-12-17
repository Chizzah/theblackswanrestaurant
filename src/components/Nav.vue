<template>
  <header class="md:text-xl">
    <nav class="absolute top-0 left-0 z-40 flex items-center justify-between w-full py-2 text-yellow-700 bg-transparent">
      <div class="flex flex-col items-center justify-between py-2">
        <g-link to="/"><h1 class="mx-8 uppercase md:text-3xl">The black swan</h1></g-link>
      </div>
      <div class="hidden md:uppercase md:font-semibold md:flex md:text-md md:items-center">
        <ul class="mr-4" v-for="menuItem in menuItems" :key="menuItem.title">
          <li class="md:px-2">
            <g-link class="hover:text-yellow-600" :to="menuItem.route"><h2>{{ menuItem.title }}</h2></g-link>
          </li>
        </ul>
        <g-link to="/reservetable"><button class="px-4 py-3 mr-4 mr-8 text-sm font-semibold text-gray-100 bg-red-700 shadow-md rounded-xl focus:outline-none">Make A Reservation</button></g-link>
      </div>
      <div class="px-4 py-2 md:hidden">
        <button @click="isOpen = !isOpen" type="button" class="block focus:outline-none">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="1" y1="12" x2="21" y2="12"></line><line x1="1" y1="6" x2="21" y2="6"></line><line x1="1" y1="18" x2="21" y2="18"></line></svg>
        </button>
      </div>
    </nav>
    <nav :class="isOpen ? 'block' : 'hidden'" class="z-50 flex flex-col items-center justify-center block w-full pt-16 pb-4 text-sm font-semibold text-yellow-700 uppercase bg-gray-900 md:p-0">
      <div class="mb-2 ml-8">
        <ul class="rounded list-reset md:hidden" v-for="menuItem in menuItems" :key="menuItem.title">
          <li class="py-2">
            <g-link class="hover:text-yellow-600" :to="menuItem.route">{{ menuItem.title }}</g-link>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      menuItems: [
        { title:'Home', route:'/' },
        { title:'About', route:'/about' },
        { title:'Menu', route:'/menu' },
        { title:'Events', route:'/events' },
        { title:'Gallery', route:'/gallery' },
        { title:'Blog', route:'/blog' },
        { title:'Contact', route:'/Contact' }
      ],
      isOpen: false,
    }
  }
}
</script>