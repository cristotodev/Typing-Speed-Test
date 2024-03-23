<script setup lang="ts">
import { ref, watch } from 'vue'

defineProps({
  disableText: {
    type: Boolean,
    required: true
  }
})

const startTime = ref(false)

const emit = defineEmits(['start-time'])

watch(startTime, (_newValue, _oldValue) => {
  emit('start-time')
})

const keyPressed = (_e: KeyboardEvent) => {
  if (!startTime.value) startTime.value = true

  //TODO Ver como gestionar las palabras
  //Cuando sea espacio tachar en color la palabra si acertó o en rojo si falló
}
</script>

<template>
  <input
    type="text"
    @keyup="keyPressed"
    class="w-2/4 rounded text-4xl font-thin shadow-2xl p-10 focus:outline-none border-none"
    placeholder="El tiempo empieza cuando escribas"
    :disabled="disableText"
  />
</template>
