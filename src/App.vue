<script setup lang="ts">
import Menu from '@/components/Menu.vue'
import Footer from '@/components/Footer.vue'
import BoxCount from '@/components/Box-count.vue'
import BoxTime from '@/components/Box-time.vue'
import InputText from '@/components/Input-text.vue'
import DividerWave from '@/components/divider-wave.vue'
</script>

<template>
  <Menu />
  <main>
    <div class="pb-10 pt-32 bg bg-[#ffd700]">
      <div class="text-center">
        <h1 class="text-1xl tracking-wide">Typing Speed Test</h1>
        <h2 class="text-6xl mt-0 tracking-wider animate-fade-in animate-delay-300 animate-duration-slow">Test your typing skills</h2>
      </div>
      <div class="flex flex-col-reverse md:flex-row justify-center items-center md:mt-0">
        <BoxTime :time="60" />
        <div class="flex justify-center">
          <BoxCount text="Palabras" />
          <BoxCount text="Caracteres" />
          <BoxCount text="% Precisión" />
        </div>
      </div>
    </div>
    <DividerWave />
    <div class="flex items-center justify-center w-full">
      <InputText />
    </div>
  </main>
  <Footer />
</template>

<style>
body {
  margin: 0;
}
</style>



