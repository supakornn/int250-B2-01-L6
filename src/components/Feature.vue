<script setup></script>

<template>
  <!-- Task 3.1: Feature section wrapper -->
  <section>
    <!-- Task 3.2: Feature container - relative, responsive, flex, stacked mobile / side-by-side desktop -->
    <div
      class="relative @container flex flex-col max-w-6xl mx-auto my-24 px-6 text-gray-800
        md:flex-row md:px-0"
    >
      <!-- Task 3.3: Feature image -->
      <img
        src="@/assets/desktop/image-interactive.jpg"
        alt="Interactive VR"
        class="w-full md:w-auto"
      />

      <!-- Task 3.4: Text container - overlays image on desktop -->
      <div class="top-48 pr-0 bg-white md:absolute md:right-0 md:py-20 md:pl-20">
        <!-- Task 3.5: Heading - responsive size, alignment, uppercase -->
        <h2
          class="max-w-lg mt-10 mb-6 font-sans text-4xl text-center text-gray-800 uppercase
            md:text-5xl md:mt-0 md:text-left"
        >
          The leader in interactive VR
        </h2>

        <!-- Task 3.6: Paragraph - centered mobile, left-aligned desktop -->
        <p class="max-w-md text-center text-gray-600 md:text-left">
          Founded in 2011, Loopstudios has been producing world-class virtual reality projects for
          some of the best companies around the globe. Our award-winning creations have transformed
          businesses through digital experiences that bind to their brand.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
