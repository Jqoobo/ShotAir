<template>
  <div class="bg-[#F8F8F8] h-[100vh]">
    <TopNav />
    <div class="flex justify-between mx-auto w-fullpx-2 max-w-[500px]">
      <slot />
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
</script>
