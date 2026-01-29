<script setup>
import Navigation from "@/components/navigation/Navigation.vue";

const socialLinks = [
  { label: "Facebook", icon: "/icons/icon-facebook.svg" },
  { label: "Twitter", icon: "/icons/icon-twitter.svg" },
  { label: "Pinterest", icon: "/icons/icon-pinterest.svg" },
  { label: "Instagram", icon: "/icons/icon-instagram.svg" },
];
</script>

<template>
  <footer class="bg-black py-14 md:py-11 xl:pb-8">
    <div class="mx-auto text-white max-w-317.5 px-14 md:px-20">
      <div
        class="grid gap-10 text-center footer-grid md:grid-cols-2 md:gap-y-6 md:text-left"
      >
        <div
          class="[grid-area:logo] w-36 h-6 justify-self-center md:justify-self-start"
        >
          <img src="/images/logo.svg" alt="Logo" class="w-full" />
        </div>
        <Navigation class="[grid-area:nav]" />
        <div
          class="[grid-area:right] flex flex-col items-center gap-4 md:gap-6 md:items-end"
        >
          <div class="flex gap-4">
            <a
              v-for="item in socialLinks"
              :key="item.label"
              href="#"
              :aria-label="item.label"
              class="link-underline"
            >
              <img :src="item.icon" :alt="item.label" />
            </a>
          </div>

          <div class="text-center md:text-right">
            <p class="text-white/50 font-sans text-[15px] leading-6.5">
              © 2021 Loopstudios. All rights reserved.
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
