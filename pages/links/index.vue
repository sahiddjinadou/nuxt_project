<template>
  <div class="max-w-[80rem] mx-auto">
    <nav class="flex items-center justify-between">
      <h1 class="text-green-500 text-2xl font-bold p-4"> Mes liens </h1>
      <SearchInput  :modelValue="search"/>
      <NuxtLink to="/links/create" class="bg-gray-800 text-white p-2 rounded capitalize transition hover:bg-gray-500"> creer un lien</NuxtLink>
    </nav>
    <table class="w-full border text-sm text-left text-gray-500 ">
      <thead class="text-xs text-gray-700 uppercase bg-gray-50">
        <tr >
          <th > Lien Complet</th>
          <th > Lien Court </th>
          <th > Nbrs Vues</th>
          <th > Supprimer </th>
          <th > Editer </th>
          <th  aria-label="Rafraichir"> 
            <Icon name="material-symbols:directory-sync" />
          </th>
        </tr>
      </thead>
      <tbody  >
        <tr v-for="link in links" :key="link.id" class="bg-white border-b">
          <td>
            <a :href="link.full_links" target="_blank">
              {{ link.full_links }}
            </a>
          </td>
          <td>
            <a :href="`${useRuntimeConfig().public.appUrl}/${link.short_links}`">
              {{ `${useRuntimeConfig().public.appUrl.replace(/^http(s?):\/\//, "")}/${link.short_links}` }}
            </a>
          </td>
          <td>
            {{ link.view }}
          </td>
          <td>
           <button>
            <Icon name="mdi:trash"/>
           </button>
          </td>
          <td>
            <NuxtLink :to="`/links/${link.id}`">
              <Icon name="material-symbols:edit-square"/>
            </NuxtLink>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script lang="ts" setup>
const links = [
  {
    short_links: "fsd3f2ds",
    full_links: "https://youtube.com",
    view: 32,
    id: 1,
  },
  {
    short_links: "fsd3f2sds",
    full_links: "https://w3school.com",
    view: 13,
    id: 2,
  },
  {
    short_links: "fszfjk3f2ds",
    full_links: "https://devdocs.io/",
    view: 20,
    id: 3,
  },
];

const search = ref<String>("")
</script>

<style scoped>
th{
  @apply px-6 py-3
}
td{
  @apply px-6 py-4
}
</style>