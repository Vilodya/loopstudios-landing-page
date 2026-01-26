<script setup lang="ts">
import CreationCard from '@/components/cards/CreationCard.vue';

const creations = [
  { title: 'Deep earth', desktop: '/images/desktop/image-deep-earth.jpg', mobile: '/images/mobile/image-deep-earth.jpg' },
  { title: 'Night arcade', desktop: '/images/desktop/image-night-arcade.jpg', mobile: '/images/mobile/image-night-arcade.jpg' },
  { title: 'Soccer team VR', desktop: '/images/desktop/image-soccer-team.jpg', mobile: '/images/mobile/image-soccer-team.jpg' },
  { title: 'The grid', desktop: '/images/desktop/image-grid.jpg', mobile: '/images/mobile/image-grid.jpg' },
  { title: 'From up above VR', desktop: '/images/desktop/image-from-above.jpg', mobile: '/images/mobile/image-from-above.jpg' },
  { title: 'Pocket borealis', desktop: '/images/desktop/image-pocket-borealis.jpg', mobile: '/images/mobile/image-pocket-borealis.jpg' },
  { title: 'The curiosity', desktop: '/images/desktop/image-curiosity.jpg', mobile: '/images/mobile/image-curiosity.jpg' },
  { title: 'Make it fisheye', desktop: '/images/desktop/image-fisheye.jpg', mobile: '/images/mobile/image-fisheye.jpg' },
]
</script>

<template>
  <section class="pt-12 xl:pt-22.5 pb-24 md:pb-22 xl:pb-45">
    <div class="page-container">
      <div class="flex items-center justify-center lg:gap-6 lg:justify-between">
        <h2 class="text-[32px] leading-none uppercase font-heading md:text-5xl">
          Our creations
        </h2>
        <a
          href="#"
          class="hidden lg:inline-block border border-black text-sm leading-none py-3 px-10 uppercase tracking-[5px]
                 hover:bg-black hover:text-white transition"
        >
          See all
        </a>
      </div>
      <div class="grid gap-4 mt-12 md:mt-8 xl:mt-20 md:grid-cols-2 lg:gap-6 lg:grid-cols-4">
        <CreationCard
          v-for="item in creations"
          :key="item.title"
          :title="item.title"
          :desktop="item.desktop"
          :mobile="item.mobile"
        />
      </div>
      <div class="flex justify-center mt-8 lg:hidden">
        <a
          href="#"
          class="inline-block border border-black text-sm leading-none py-3 px-10 uppercase tracking-[5px]
                 hover:bg-black hover:text-white transition"
        >
          See all
        </a>
      </div>
    </div>
  </section>
</template>
