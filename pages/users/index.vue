<template>
  <div>
    <div class="my-10">
      <h1 class="text-bold text-3xl text-blue-600 text-center">Utilisateurs</h1>
    </div>

    <div v-if="users.length === 0">
      <p class="text-xl text-center">Désolé, nous n'avons pas encore d'utilisateurs à afficher ici...</p>
    </div>

    <div v-else v-for="user in users" :key="user.id" class="px-96">
      <nuxt-link :to="`/users/${user.id}`">
        <div class="border-2 border-black flex items-center justify-center mb-5 py-2">
          <ul>
            <li>Nom : {{ user.name }}</li>
            <li>Pseudo : {{ user.username }}</li>
            <li>Email : {{ user.email }}</li>
          </ul>
        </div>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name : 'Users',
  data(){
    return {
      users : []
    }
  },
  async fetch() {
    this.users = await fetch(
      'https://jsonplaceholder.typicode.com/users'
    ).then(res => res.json())
  },
   head: {
    title: `NuxtBlog | Users`
  }

}
</script>