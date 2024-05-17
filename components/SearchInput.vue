<template>
  <div>
    <label class="border flex items-center bg-gray-50 ">
      <Icon name="material-symbols:search" class="absolute top-[50] translate-y-[50] w-6 h-6" />
      <input type="text" placeholder="Rechercher un lien" class=" pl-10 p-2 rounded " v-model="modelValue">
    </label>
    <p> {{ modelValue }}</p>
  </div>
</template>

<script lang="ts" setup>
 const modelValue = defineModel()
</script>

<style>

</style>