<script setup lang="ts">
import GithubIcon from '@/icons/Github-icon.vue'
import InstagramIcon from '@/icons/Instagram-icon.vue'
import XIcon from '@/icons/X-icon.vue'
import YoutubeIcon from '@/icons/Youtube-icon.vue'
import TiktokIcon from '@/icons/Tiktok-icon.vue'
</script>

<template>
  <nav>
    <ul
      class="flex flex-row items-center gap-x-6 list-none"
      aria-label="redes sociales y botón para alternar tema"
    >
      <li>
        <a
          target="_blank"
          rel="noopener"
          aria-label="Instagram de cristoto.dev, se abrirá en una nueva pestaña"
          href="https://www.instagram.com/cristoto.dev/"
          class="inline-block any-hover:scale-125 any-hover:opacity-70 motion-safe:transition motion-reduce:any-hover:scale-100"
        >
          <InstagramIcon classes="transition duration-150 ease-in-out" />
        </a>
      </li>
      <li>
        <a
          target="_blank"
          rel="noopener"
          aria-label="X de cristoto.dev, se abrirá en una nueva pestaña"
          href="https://twitter.com/cristotodev"
        >
          <XIcon classes="text-black" />
        </a>
      </li>
      <li>
        <a
          target="_blank"
          rel="noopener"
          aria-label="GitHub de cristoto.dev, se abrirá en una nueva pestaña"
          href="https://github.com/cristotodev"
        >
          <GithubIcon classes="text-black" />
        </a>
      </li>
      <li>
        <a
          target="_blank"
          rel="noopener"
          aria-label="Youtube de cristoto.dev, se abrirá en una nueva pestaña"
          href="https://www.youtube.com/channel/UCwrDxf6HdbM6yfZjqUMOuyg"
        >
          <YoutubeIcon classes="text-black" />
        </a>
      </li>
      <li>
        <a
          target="_blank"
          rel="noopener"
          aria-label="TikTok de cristoto.dev, se abrirá en una nueva pestaña"
          href="https://www.tiktok.com/@cristoto.dev"
        >
          <TiktokIcon classes="text-black" />
        </a>
      </li>
    </ul>
  </nav>
</template>
