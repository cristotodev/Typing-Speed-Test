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
            {{ time }}
        </div>
      </div>
</template>