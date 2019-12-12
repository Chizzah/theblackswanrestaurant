<template>
  <layout>
    <section class="flex flex-col justify-center items-center text-center">
    <h1 class="my-8 text-lg uppercase font-bold">Reserve a table at the best <br> restaurant in Oudtshoorn</h1>
    <h3 class="text-xs font-semibold">We'll call you back with the closest <br> availablity to your booking.</h3>
    </section>
    <section class="my-12 mx-auto w-88">
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