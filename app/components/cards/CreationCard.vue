<script setup lang="ts">
defineProps<{
  title: string
  desktop: string
  mobile: string
}>()
</script>

<template>
  <a
    href="#"
    class="group relative block h-32 overflow-hidden md:h-[450px] md:max-w-64"
  >
    <div
      class="absolute inset-0 bg-cover bg-center
             md:bg-[image:var(--bg-desktop)]
             bg-[image:var(--bg-mobile)]"
      :style="{
        '--bg-mobile': `url(${mobile})`,
        '--bg-desktop': `url(${desktop})`,
      }"
    ></div>

    <div class="absolute inset-0 bg-black/35 group-hover:bg-white/60 transition"></div>

    <p
      class="absolute bottom-5 left-5 right-5 text-white
             font-heaading uppercase text-2xl leading-tight
             group-hover:text-black transition md:bottom-10 md:left-10 md:right-10"
    >
      {{ title }}
    </p>
  </a>
</template>
