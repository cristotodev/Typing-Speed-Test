<script setup lang="ts">
defineProps({
  text: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="text-center mx-2">
    <div class="bg-white mb-1 text-3xl w-20 h-20 rounded-3xl items-center flex justify-center">
      0
    </div>
    <div class="text-sm">{{ text }}</div>
  </div>
</template>