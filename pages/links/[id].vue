<template>
  <div class="mx-auto max-w-md">
    <h1 class="text-3xl font-bold text-gray-500">Modifier le lien</h1>
    <GoBack/>
    <form>
      <label>
        <div>Lien Court</div>
        <input type="text" />
      </label>
      <label>
        <div>Lien Complet</div>
        <input type="text" />
      </label>
      <button class=" p-2 border bg-gray-300">Modifier le lien</button>
    </form>
  </div>
</template>

<script lang="ts" setup>
</script>

<style>
label {
  @apply block mb-2 text-sm font-medium text-gray-900;
}

input {
  @apply bg-gray-50  text-gray-900 text-sm rounded focus:ring-blue-50 block w-full p-2.5;
}
</style>