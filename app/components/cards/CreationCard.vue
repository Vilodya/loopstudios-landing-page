<script setup lang="ts">
defineProps<{
  title: string[];
  desktop: string;
  mobile: string;
}>();
</script>

<template>
  <a
    href="#"
    class="group w-full relative block h-30 overflow-hidden lg:h-112.5 lg:max-w-64"
  >
    <div
      class="absolute inset-0 bg-cover bg-center lg:bg-[image:var(--bg-desktop)] bg-[image:var(--bg-mobile)]"
      :style="{
        '--bg-mobile': `url(${mobile})`,
        '--bg-desktop': `url(${desktop})`,
      }"
    ></div>

    <div
      class="absolute inset-0 transition-opacity duration-300 opacity-100 pointer-events-none gradient-black-vertical group-hover:opacity-0"
    ></div>

    <div
      class="absolute inset-0 transition-opacity duration-300 bg-white opacity-0 pointer-events-none group-hover:opacity-75"
    ></div>

    <p
      class="absolute z-10 text-2xl xl:text-[32px] leading-none text-white uppercase transition bottom-5 left-5 font-heading group-hover:text-black md:left-9 lg:left-10 lg:bottom-8"
    >
      <span v-for="(line, i) in title" :key="i" class="block">
        {{ line }}
      </span>
    </p>
  </a>
</template>
