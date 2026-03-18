<script setup>
import { ref } from 'vue';

const menuItems = [
  { name: 'About', link: '#' },
  { name: 'Careers', link: '#' },
  { name: 'Events', link: '#' },
  { name: 'Products', link: '#' },
  { name: 'Support', link: '#' },
];

const mobileMenuOpen = ref(false);

function toggleMenu() {
  mobileMenuOpen.value = !mobileMenuOpen.value;
}
</script>

<template>
  <!-- Task 2.1: Hero section wrapper with responsive background -->
  <section
    class="bg-[url(@/assets/mobile/image-hero.jpg)] bg-no-repeat bg-cover
      md:bg-[url(@/assets/desktop/image-hero.jpg)] md:bg-no-repeat md:bg-cover"
  >
    <!-- Task 2.2: Container layout -->
    <div class="@container max-w-6xl mx-auto px-6 py-12">
      <!-- Task 2.3: Navigation bar -->
      <nav class="flex items-center justify-between font-bold text-white">
        <!-- Logo -->
        <img src="@/assets/logo.svg" alt="Loopstudios logo" />

        <!-- Challenge: Hamburger button (mobile only) -->
        <button class="md:hidden focus:outline-none" @click="toggleMenu" aria-label="Toggle menu">
          <img v-if="!mobileMenuOpen" src="@/assets/icon-hamburger.svg" alt="Open menu" />
          <img v-else src="@/assets/icon-close.svg" alt="Close menu" />
        </button>

        <!-- Task 2.4: Desktop menu (md+ only) -->
        <div class="hidden h-10 font-sans md:flex md:items-center md:space-x-8">
          <!-- Task 2.5: Menu links with hover underline -->
          <div v-for="item in menuItems" :key="item.name" class="group">
            <a :href="item.link" class="text-white">{{ item.name }}</a>
            <div
              class="mx-2 border-b border-transparent group-hover:border-white transition-all
                duration-200"
            ></div>
          </div>
        </div>
      </nav>

      <!-- Challenge: Mobile navigation menu -->
      <div v-if="mobileMenuOpen" class="md:hidden mt-8 flex flex-col space-y-6 font-sans">
        <a
          v-for="item in menuItems"
          :key="item.name"
          :href="item.link"
          class="text-white text-2xl font-bold uppercase"
        >
          {{ item.name }}
        </a>
      </div>

      <!-- Task 2.6: Hero headline text box -->
      <div class="mt-24 mb-24 mx-2 border border-white p-6 md:max-w-lg md:mt-32 md:p-10">
        <h1 class="text-white font-sans font-light text-4xl uppercase md:text-6xl leading-tight">
          Immersive experiences that deliver
        </h1>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
