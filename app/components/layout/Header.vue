<script setup lang="ts">
import { ref, watch } from 'vue'

const isOpen = ref(false)

// // блокировка скролла при открытом меню
// watch(isOpen, (v) => {
//   if (process.client) document.documentElement.style.overflow = v ? 'hidden' : ''
// })
</script>

<template>
  <header class="absolute inset-x-0 top-0 z-50">
    <div class="container flex items-center justify-between py-10">
      <NuxtLink to="/" aria-label="Loopstudios home">
        <img src="/icons/logo.svg" alt="Loopstudios" class="h-6 md:h-7" />
      </NuxtLink>

      <!-- Desktop nav -->
      <nav class="hidden md:block">
        <ul class="flex items-center gap-8 text-white">
          <li><a class="hover:underline underline-offset-8" href="#">About</a></li>
          <li><a class="hover:underline underline-offset-8" href="#">Careers</a></li>
          <li><a class="hover:underline underline-offset-8" href="#">Events</a></li>
          <li><a class="hover:underline underline-offset-8" href="#">Products</a></li>
          <li><a class="hover:underline underline-offset-8" href="#">Support</a></li>
        </ul>
      </nav>

      <!-- Burger -->
      <button
        class="md:hidden"
        type="button"
        aria-label="Open menu"
        @click="isOpen = true"
      >
        <img src="/icons/icon-hamburger.svg" alt="" class="h-4 w-6" />
      </button>
    </div>

    <!-- Mobile menu -->
    <div v-if="isOpen" class="fixed inset-0 z-50 bg-black">
      <div class="container flex items-center justify-between py-10">
        <img src="/icons/logo.svg" alt="Loopstudios" class="h-6" />

        <button type="button" aria-label="Close menu" @click="isOpen = false">
          <img src="/icons/icon-close.svg" alt="" class="h-5 w-5" />
        </button>
      </div>

      <nav class="container mt-10">
        <ul class="space-y-6 text-white text-2xl font-[var(--font-heading)] uppercase">
          <li><a href="#" @click="isOpen = false">About</a></li>
          <li><a href="#" @click="isOpen = false">Careers</a></li>
          <li><a href="#" @click="isOpen = false">Events</a></li>
          <li><a href="#" @click="isOpen = false">Products</a></li>
          <li><a href="#" @click="isOpen = false">Support</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>
