<template>
  <div class="border-b-2 border-gray-300">
    <ul class="flex justify-between items-center w-full px-5 py-1">
      <li><nuxt-link to="/users" class="text-2xl">Utilisateurs</nuxt-link></li>
      <li><nuxt-link to="/about" class="text-2xl">About</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
export default {
  name : 'Nav',
}
</script>