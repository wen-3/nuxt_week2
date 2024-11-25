<script setup>
const route = useRoute();
</script>

<template> 
  <div>
    <h2>進入課程：{{ route.params.id }}</h2>
  </div>
</template>

<style>
</style>