<script setup lang="ts">
defineProps({
  time: {
    type: Number,
    required: true
  }
})
</script>

<template>
  <div class="mt-2 md:mt-0 md:mr-8 rounded-full">
    <div class="bg-white mb-1 text-3xl w-24 h-24 rounded-full items-center flex justify-center">
      <span class="-mt-4">{{ time }}</span>
      <div class="absolute flex text-xs pt-10">segundos</div>
    </div>
  </div>
</template>
