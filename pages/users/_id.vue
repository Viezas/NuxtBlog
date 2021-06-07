<template>
  <div>
    <div class="my-10">
      <h1 class="text-bold text-3xl text-blue-600 text-center">Utilisateur</h1>
    </div>

    <div v-if="user.length === 0">
      <p class="text-xl text-center">Mauvais identifiant fournit !</p>
    </div>

    <div v-else class="px-96">
      <User :user="user"/>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      user : []
    }
  },
  async asyncData({ params, $http }) {
    const user = await $http.$get(`https://jsonplaceholder.typicode.com/users/${params.id}`)
    return { user }
  },
  head() {
    return {title: `NuxtBlog | ${this.user.name}`}
  }
}
</script>