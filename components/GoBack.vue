<template>
  <div>
    <a href="#" class="text-sm mb-5 italic flex items-center gap-3"
    @click.prevent="useRouter().back()">
      <Icon name="material-symbols:arrow-circle-left-outline"/>
      <span>Retour</span> 
    </a>
  </div>
</template>

<script lang="ts" setup>

</script>

<style>

</style>