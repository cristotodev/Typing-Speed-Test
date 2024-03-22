<script setup lang="ts">
import { ref } from 'vue'
import SocialButtons from '@/components/SocialButtons.vue'

const year = ref(new Date().getFullYear())
</script>

<template>
  <footer class="flex justify-center">
    <div class="flex flex-col gap-4 text-center md:flex-row lg:gap-6 items-center">
      &copy; {{ year }} Cristoto.dev <span aria-hidden="true" class="hidden md:inline">|</span
      ><br aria-hidden="true" class="block md:hidden" />
      Todos los derechos reservados.
    </div>

    <SocialButtons />
  </footer>
</template>
