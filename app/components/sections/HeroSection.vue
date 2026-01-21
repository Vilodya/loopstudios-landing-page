<template>
  <section
    class="relative min-h-[650px] bg-cover bg-center
           bg-[url('/images/mobile/image-hero.jpg')]
           md:bg-[url('/images/desktop/image-hero.jpg')]"
  >
    <!-- затемнение -->
    <div class="absolute inset-0 bg-black/40"></div>

    <div class="relative container flex min-h-[650px] items-center">
      <h1
        class="max-w-[650px] border border-white p-6 text-white
               font-[var(--font-heading)] uppercase
               text-[40px] leading-[1] md:text-7xl"
      >
        Immersive experiences that deliver
      </h1>
    </div>
  </section>
</template>
