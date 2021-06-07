<template>
  <div>
    <h1 v-if="error.statusCode === 404" class="text-3xl font-bold text-red-600 text-center my-5">Page not found</h1>
    <h1 v-else class="text-3xl font-bold text-red-600 text-center my-5">An error occurred</h1>
    <div class="w-full flex items-center justify-center">
      <NuxtLink to="/" class="text-center text-xl text-blue-600 border-b-2 border-blue-600">Home page</NuxtLink>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['error'],
    layout: 'error'
  }
</script>