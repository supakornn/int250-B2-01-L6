<script setup>
const footerLinks = [
  { name: 'About', link: '#' },
  { name: 'Careers', link: '#' },
  { name: 'Events', link: '#' },
  { name: 'Products', link: '#' },
  { name: 'Support', link: '#' },
];

const socialIcons = [
  {
    name: 'Facebook',
    icon: new URL('@/assets/icon-facebook.svg', import.meta.url).href,
    link: '#',
  },
  { name: 'Twitter', icon: new URL('@/assets/icon-twitter.svg', import.meta.url).href, link: '#' },
  {
    name: 'Pinterest',
    icon: new URL('@/assets/icon-pinterest.svg', import.meta.url).href,
    link: '#',
  },
  {
    name: 'Instagram',
    icon: new URL('@/assets/icon-instagram.svg', import.meta.url).href,
    link: '#',
  },
];
</script>

<template>
  <!-- Challenge: Footer section -->
  <footer class="bg-black text-white">
    <div
      class="max-w-6xl mx-auto px-6 py-10 flex flex-col items-center gap-8 md:flex-row
        md:justify-between md:items-start md:px-0"
    >
      <!-- Left: Logo + Nav links -->
      <div class="flex flex-col items-center gap-6 md:items-start">
        <!-- Logo -->
        <a href="#">
          <img src="@/assets/logo.svg" alt="Loopstudios logo" class="h-6" />
        </a>

        <!-- Footer nav links -->
        <nav class="flex flex-col items-center gap-4 md:flex-row md:gap-8">
          <div v-for="link in footerLinks" :key="link.name" class="group">
            <a
              :href="link.link"
              class="text-sm text-white hover:text-gray-300 transition-colors duration-200"
            >
              {{ link.name }}
            </a>
            <div
              class="mx-2 border-b border-transparent group-hover:border-white transition-all
                duration-200"
            ></div>
          </div>
        </nav>
      </div>

      <!-- Right: Social icons + copyright -->
      <div class="flex flex-col items-center gap-4 md:items-end">
        <!-- Social media icons -->
        <div class="flex items-center gap-4">
          <a
            v-for="social in socialIcons"
            :key="social.name"
            :href="social.link"
            :aria-label="social.name"
            class="group"
          >
            <img
              :src="social.icon"
              :alt="social.name"
              class="h-5 opacity-100 hover:opacity-60 transition-opacity duration-200"
            />
          </a>
        </div>

        <!-- Copyright -->
        <p class="text-sm text-gray-400">&copy; 2021 Loopstudios. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped></style>
