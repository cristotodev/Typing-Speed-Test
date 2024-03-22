<script setup>
import { computed } from 'vue'
const props = defineProps({
  minute: {
    type: Number,
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
  <div @click="emitEvent" class="cursor-pointer bg-[#ffd700] hover:bg-[#b29600] p-3 rounded-2xl">
    {{ minute }} {{ text }}
  </div>
</template>
