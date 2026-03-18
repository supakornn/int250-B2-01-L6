<script setup>
const creations = [
  {
    name: 'Deep Earth',
    desktopImg: new URL('@/assets/desktop/image-deep-earth.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-deep-earth.jpg', import.meta.url).href,
  },
  {
    name: 'Night Arcade',
    desktopImg: new URL('@/assets/desktop/image-night-arcade.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-night-arcade.jpg', import.meta.url).href,
  },
  {
    name: 'Soccer Team VR',
    desktopImg: new URL('@/assets/desktop/image-soccer-team.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-soccer-team.jpg', import.meta.url).href,
  },
  {
    name: 'The Grid',
    desktopImg: new URL('@/assets/desktop/image-grid.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-grid.jpg', import.meta.url).href,
  },
  {
    name: 'From Up Above VR',
    desktopImg: new URL('@/assets/desktop/image-from-above.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-from-above.jpg', import.meta.url).href,
  },
  {
    name: 'Pocket Borealis',
    desktopImg: new URL('@/assets/desktop/image-pocket-borealis.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-pocket-borealis.jpg', import.meta.url).href,
  },
  {
    name: 'The Curiosity',
    desktopImg: new URL('@/assets/desktop/image-curiosity.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-curiosity.jpg', import.meta.url).href,
  },
  {
    name: 'Make It Fisheye',
    desktopImg: new URL('@/assets/desktop/image-fisheye.jpg', import.meta.url).href,
    mobileImg: new URL('@/assets/mobile/image-fisheye.jpg', import.meta.url).href,
  },
];
</script>

<template>
  <!-- Task 4.1: Section container -->
  <section>
    <div class="@container max-w-6xl mx-auto my-32 px-6 text-gray-800 md:px-0">
      <!-- Task 4.2: Creations header row -->
      <div class="flex flex-col items-center mb-10 md:flex-row md:justify-between">
        <!-- Task 4.3: Section title -->
        <h2 class="text-4xl text-center uppercase text-gray-800 md:text-left md:text-5xl">
          Our Creations
        </h2>

        <!-- Task 4.4: Top "See All" button (desktop only) -->
        <button
          class="hidden px-10 py-2 my-0 font-bold tracking-widest uppercase border-2 border-black
            hover:bg-black hover:text-white transition-colors duration-200 md:block"
        >
          See All
        </button>
      </div>

      <!-- Task 4.5: Item container -->
      <div
        class="flex flex-col w-full gap-y-6 text-2xl text-white uppercase md:flex-row md:gap-y-0
          md:gap-x-8"
      >
        <!-- Task 4.6: Item card -->
        <div
          v-for="item in creations"
          :key="item.name"
          class="group relative overflow-hidden md:w-1/4"
        >
          <!-- Task 4.7: Desktop image -->
          <img
            :src="item.desktopImg"
            :alt="item.name"
            class="hidden w-full transition duration-200 group-hover:scale-110 md:block"
          />

          <!-- Task 4.7: Mobile image -->
          <img :src="item.mobileImg" :alt="item.name" class="w-full md:hidden" />

          <!-- Task 4.8: Gradient overlay -->
          <div
            class="absolute inset-0 bg-linear-to-b from-transparent to-gray-800
              hover:from-white/30 hover:to-white/60 group-hover:opacity-80 transition-all
              duration-200"
          ></div>

          <!-- Task 4.8: Card title -->
          <h5
            class="absolute bottom-4 left-0 px-6 w-52 transition duration-200 group-hover:scale-110
              group-hover:text-black md:bottom-8 md:px-10"
          >
            {{ item.name }}
          </h5>
        </div>
      </div>

      <!-- Task 4.9: Bottom "See All" button (mobile only) -->
      <div class="flex flex-col items-center mt-10 md:hidden">
        <button
          class="w-full px-10 py-2 my-0 font-bold tracking-widest uppercase border-2 border-black
            hover:bg-black hover:text-white transition-colors duration-200 md:hidden"
        >
          See All
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
