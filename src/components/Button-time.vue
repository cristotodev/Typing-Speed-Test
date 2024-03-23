<script setup>
import { computed } from 'vue'
const props = defineProps({
  minute: {
    type: Number,
    required: true
  },
  disable: {
    type: Boolean,
    required: true
  }
})

const text = computed(() => {
  return props.minute > 1 ? 'minutos' : 'minuto'
})

const emit = defineEmits(['minute-selected'])
const emitEvent = () => {
  emit('minute-selected', props.minute)
}
</script>

<template>
  <div @click="disable ? null : emitEvent" :class="disable ? 'bg-gray-200 cursor-not-allowed' : 'bg-[#ffd700] cursor-pointer hover:bg-[#b29600]'" class="p-3 rounded-2xl">
    {{ minute }} {{ text }}
  </div>
</template>
