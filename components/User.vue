<template>
  <div>
    <div class="border-2 border-black flex items-center justify-center mb-5 py-2">
      <ul>
        <li class="border-b-2 border-blue-600 mb-2">Nom : {{ user.name }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Pseudo : {{ user.username }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Email : {{ user.email }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Adresse : {{ user.address.street }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Ville : {{ user.address.city }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Code postal : {{ user.address.zipcode }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Appartement : {{ user.address.suite }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Site Web : {{ user.website }}</li>
        <li class="border-b-2 border-blue-600 mb-2">Entreprise : {{ user.company.name }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name : 'User',
  props : ['user']
}
</script>