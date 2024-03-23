<script setup lang="ts">
import { ref, watch } from 'vue'
import Menu from '@/components/Menu.vue'
import Footer from '@/components/Footer.vue'
import BoxCount from '@/components/Box-count.vue'
import BoxTime from '@/components/Box-time.vue'
import InputText from '@/components/Input-text.vue'
import DividerWave from '@/components/divider-wave.vue'
import ButtonTime from '@/components/Button-time.vue'

const seconds = ref(60)
const disableText = ref(false)
const disableButtons = ref(false)
let intervalId: number | undefined = undefined

const timeSelectedEvent = (minute: number) => {
  seconds.value = minute * 60
}

watch(seconds, (newValue, _oldValue) => {
  if (newValue <= 0 && intervalId !== undefined) {
    disableText.value = true
    clearInterval(intervalId)
    intervalId = undefined
  }
})

const handleStartTime = () => {
  disableButtons.value = true;
  if (intervalId === undefined) {
    intervalId = setInterval(() => {
      console.log('ee')
      seconds.value--
    }, 1000)
  }
}
</script>

<template>
  <Menu />
  <main>
    <div class="pb-10 pt-32 bg bg-[#ffd700]">
      <div class="text-center">
        <h1 class="text-1xl tracking-wide">Typing Speed Test</h1>
        <h2
          class="text-6xl mt-0 tracking-wider animate-fade-in animate-delay-300 animate-duration-slow"
        >
          Test your typing skills
        </h2>
      </div>
      <div class="flex flex-col-reverse md:flex-row justify-center items-center md:mt-0">
        <BoxTime :time="seconds" />
        <div class="flex justify-center">
          <BoxCount text="Palabras" />
          <BoxCount text="Caracteres" />
          <BoxCount text="% Precisión" />
        </div>
      </div>
    </div>
    <DividerWave />
    <div class="flex justify-center space-x-14 pb-10">
      <ButtonTime @minute-selected="timeSelectedEvent" :minute="1" :disable="disableButtons"/>
      <ButtonTime @minute-selected="timeSelectedEvent" :minute="3" :disable="disableButtons"/>
      <ButtonTime @minute-selected="timeSelectedEvent" :minute="5" :disable="disableButtons"/>
    </div>
    <div class="flex items-center justify-center">
      <InputText @start-time="handleStartTime" :disable-text="disableText" />
    </div>
    <div
      class="flex justify-center p-12 border-4 bg-slate-50 m-16 text-xl rounded-3xl"
    >
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nesciunt iure optio corrupti?
      Distinctio voluptatem quos hic sapiente iure deleniti quae placeat sit corrupti suscipit atque
      totam velit sequi, inventore assumenda?
    </div>
  </main>
  <Footer />
</template>

<style>
body {
  margin: 0;
}
</style>
