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
    class="group w-full relative block h-30 overflow-hidden lg:h-112.5 lg:max-w-64"
  >
    <div
      class="absolute inset-0 bg-cover bg-center
             lg:bg-[image:var(--bg-desktop)]
             bg-[image:var(--bg-mobile)]"
      :style="{
        '--bg-mobile': `url(${mobile})`,
        '--bg-desktop': `url(${desktop})`,
      }"
    ></div>

    <div class="absolute inset-0 transition bg-black/35 group-hover:bg-white/60"></div>

    <p
      class="absolute text-2xl leading-tight text-white uppercase transition bottom-5 left-5 right-5 font-heaading group-hover:text-black md:bottom-10 md:left-10 md:right-10"
    >
      {{ title }}
    </p>
  </a>
</template>
