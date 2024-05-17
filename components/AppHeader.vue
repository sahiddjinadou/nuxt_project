<template>
  <div>
    <nav
      class="bg-gray-800 text-white p-4 shadow-md shadow-gray-900 flex items-center justify-between mb-10"
    >
      <NuxtLink to="/" class="text-3xl font-bold"> URL shortify </NuxtLink>

      <div class=" flex gap-2 items-center">
        <NuxtLink to="/me" class="text-xl">Profile</NuxtLink>
        <NuxtLink to="/links/index" class="text-xl"> Mes miens</NuxtLink>
        <NuxtLink to="#" class="text-xl">About</NuxtLink>
        <NuxtLink to="#" class="p-2">
          <Icon name="mdi:logout" />
        </NuxtLink>
      </div>
    </nav>
  </div>
</template>

<script lang="ts" setup>

</script>

<style>
</style>