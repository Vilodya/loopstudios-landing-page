<script setup lang="ts">
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
  <section class="py-20 md:py-28">
    <div class="container">
      <div class="flex items-center justify-between gap-6">
        <h2 class="font-[var(--font-heading)] uppercase text-3xl md:text-5xl">
          Our creations
        </h2>

        <a
          href="#"
          class="hidden md:inline-block border border-black px-10 py-3 uppercase tracking-[.25em]
                 hover:bg-black hover:text-white transition"
        >
          See all
        </a>
      </div>

      <div class="mt-12 grid gap-6 md:grid-cols-4">
        <CreationCard
          v-for="item in creations"
          :key="item.title"
          :title="item.title"
          :desktop="item.desktop"
          :mobile="item.mobile"
        />
      </div>

      <!-- кнопка для mobile (по макету она снизу) -->
      <div class="mt-10 flex justify-center md:hidden">
        <a
          href="#"
          class="border border-black px-10 py-3 uppercase tracking-[.25em]
                 hover:bg-black hover:text-white transition"
        >
          See all
        </a>
      </div>
    </div>
  </section>
</template>
