<template>
  <div>
    <h1> Mes liens </h1>
    <table>
      <thead>
        <tr>
          <th> Lien Complet</th>
          <th> Lien Court </th>
          <th> Nbrs Vues</th>
          <th> Supprimer </th>
          <th> Editer </th>
          <th> Rafraichir</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="link in links" :key="link.id">
          <td>
            <a :href="link.full_links" target="_blank">
              {{ link.full_links }}
            </a>
          </td>
          <td>
            <a href="#">
              {{ `${useRuntimeConfig().public.appUrl}/${link.short_links}` }}
            </a>
          </td>
          <td>
            {{ link.view }}
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
</script>

<style>

</style>