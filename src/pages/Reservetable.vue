<template>
  <layout>
    <section class="flex flex-col items-center justify-center text-center">
    <h1 class="mt-20 mb-8 text-lg font-bold uppercase md:mt-40 md:text-4xl">Reserve a table at the <br> best restaurant in Oudtshoorn</h1>
    <h3 class="text-sm font-semibold md:text-2xl">We'll call you back with the closest <br> availablity to your booking.</h3>
    </section>
    <section class="mx-auto my-12 w-88">
      <Form />
    </section>
  </layout>
</template>

<script>
import Form from '~/components/Form.vue';

export default {
  components: {
    Form
  }
}
</script>

<style>

</style>