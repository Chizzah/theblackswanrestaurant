<template>
  <section>
    <section class="flex items-center justify-around py-4">
      <button @click="selectTab(0)" aria-label="Appetisers Tab Button" :class="{ 'md:bg-yellow-700 md:text-gray-100 font-bold text-yellow-700' : currentTab == 0 }" class="flex items-center justify-center w-1/4 px-4 py-3 text-sm font-semibold uppercase md:border-2 md:border-yellow-700 md:border-solid md:rounded-xl md:w-40 hover:md:bg-yellow-700 hover:md:text-gray-100 hover:font-bold focus:outline-none" tabindex="0">Appetisers</button>
      <button @click="selectTab(1)" aria-label="Mains Tab Button" :class="{ 'md:bg-yellow-700 md:text-gray-100 font-bold text-yellow-700' : currentTab == 1 }" class="flex items-center justify-center w-1/4 px-4 py-3 text-sm font-semibold uppercase md:border-2 md:border-yellow-700 md:border-solid md:rounded-xl md:w-40 hover:md:bg-yellow-700 hover:md:text-gray-100 hover:font-bold focus:outline-none">Mains</button>
      <button @click="selectTab(2)" aria-label="Specialities Tab Button" :class="{ 'md:bg-yellow-700 md:text-gray-100 font-bold text-yellow-700' : currentTab == 2 }" class="flex items-center justify-center w-1/4 px-4 py-3 text-sm font-semibold uppercase md:border-2 md:border-yellow-700 md:border-solid md:rounded-xl md:w-40 hover:md:bg-yellow-700 hover:md:text-gray-100 hover:font-bold focus:outline-none">Specialities</button>
      <button @click="selectTab(3)" aria-label="Desserts Tab Button" :class="{ 'md:bg-yellow-700 md:text-gray-100 font-bold text-yellow-700' : currentTab == 3 }" class="flex items-center justify-center w-1/4 px-4 py-3 text-sm font-semibold uppercase md:border-2 md:border-yellow-700 md:border-solid md:rounded-xl md:w-40 hover:md:bg-yellow-700 hover:md:text-gray-100 hover:font-bold focus:outline-none">Desserts</button>
    </section>

    <section v-if="currentTab == 0">
        <section>
          <h2 class="mt-12 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:mt-20 md:text-2xl">Appetisers</h2>
          <section class="md:flex md:flex-col md:justify-center md:items-center" v-for="edge in $page.appetisers.edges" :key="edge.node.id">
            <section class="flex items-center justify-between md:w-128">
              <h3 class="my-4 ml-4 font-bold md:text-left">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-bold text-yellow-700">{{ edge.node.price }}</h4>
            </section>
            <section class="flex items-center justify-center md:justify-start md:flex-col">
              <h5 class="mb-4 ml-3 text-sm font-thin md:text-lg md:w-116 w-96 md:ml-0">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
    </section>

    <section v-if="currentTab == 1">
        <section>
          <h2 class="mt-12 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:mt-20 md:text-2xl">Mains</h2>
          <section class="md:flex md:flex-col md:justify-center md:items-center" v-for="edge in $page.mains.edges" :key="edge.node.id">
            <section class="flex items-center justify-between md:w-128">
              <h3 class="my-4 ml-4 font-bold md:text-left">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-bold text-yellow-700 md:ml-12 md:mr-0">{{ edge.node.price }}</h4>
            </section>
            <section class="flex items-center justify-center md:justify-start md:flex-col">
              <h5 class="mb-4 ml-3 text-sm font-thin md:text-lg md:w-116 w-96 md:ml-0">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
    </section>

    <section v-if="currentTab == 2">
        <section>
          <h2 class="mt-12 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:mt-20 md:text-2xl">Specialities</h2>
          <section class="md:flex md:flex-col md:justify-center md:items-center" v-for="edge in $page.specialities.edges" :key="edge.node.id">
            <section class="flex items-center justify-between md:w-128">
              <h3 class="my-4 ml-4 font-bold md:text-left">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-bold text-yellow-700 md:ml-12 md:mr-0">SQ</h4>
            </section>
            <section class="flex items-center justify-center md:justify-start md:flex-col">
              <h5 class="mb-4 ml-3 text-sm font-thin md:text-lg md:w-116 w-96 md:ml-0">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
    </section>

    <section v-if="currentTab == 3">
        <section>
          <h2 class="mt-12 mb-12 text-xl font-bold text-center text-yellow-700 uppercase md:mt-20 md:text-2xl">Desserts</h2>
          <section class="md:flex md:flex-col md:justify-center md:items-center" v-for="edge in $page.desserts.edges" :key="edge.node.id">
            <section class="flex items-center justify-between md:w-128">
              <h3 class="my-4 ml-4 font-bold md:text-left">{{ edge.node.name }}</h3>
              <h4 class="mr-4 font-bold text-yellow-700 md:ml-12 md:mr-0">{{ edge.node.price }}</h4>
            </section>
            <section class="flex items-center justify-center md:justify-start md:flex-col">
              <h5 class="mb-4 ml-3 text-sm font-thin md:text-lg md:w-116 w-96 md:ml-0">{{ edge.node.description }}</h5>
            </section>
          </section>
        </section>
    </section>
  </section>
</template>

<script>
export default {
  data:() => {
    return {
      currentTab: 0
    }
  },
  methods: {
    selectTab(selectedTab) {
      this.currentTab = selectedTab
    }
  }
}
</script>