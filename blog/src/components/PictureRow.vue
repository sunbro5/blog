<script setup lang="ts">
defineProps<{
  name: string
}>()
</script>

<template>
  <div class="picture">
    <image src="{{name}}.jpg" height="300" width="200"/>
  </div>
</template>

<style scoped>


</style>
