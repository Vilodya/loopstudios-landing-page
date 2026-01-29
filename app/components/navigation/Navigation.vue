<script setup>
const navLinks = [
  { label: "About", href: "#" },
  { label: "Careers", href: "#" },
  { label: "Events", href: "#" },
  { label: "Products", href: "#" },
  { label: "Support", href: "#" },
];
</script>

<template>
  <nav
    class="flex flex-col gap-4 lg:gap-8 font-sans text-[15px] leading-relaxed md:flex-row"
  >
    <a
      v-for="item in navLinks"
      :key="item.label"
      :href="item.href"
      class="link-underline"
      >{{ item.label }}</a
    >
  </nav>
</template>
