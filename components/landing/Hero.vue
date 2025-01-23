<script>
export default {
  methods: {
    downloadCv() {
      const cvPath = '/Francisca Kipsang CV-UPDATED.pdf'; // Path to your CV file
      const link = document.createElement('a');
      link.href = cvPath;
      link.download = 'Francisca Kipsang CV-UPDATED.pdf'; // Desired file name
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    },
  },
};
</script>

<template>
  <main class="relative bg-gray-100 py-16 lg:py-24">
    <div class="container mx-auto px-6 lg:px-16 grid lg:grid-cols-2 items-center gap-12">
      <!-- Right Section: Image (comes first on mobile) -->
      <div class="relative order-1 lg:order-2">
        <div class="rounded-full overflow-hidden shadow-lg hover:shadow-2xl transition-shadow">
          <img
            src="/assets/img/WhatsApp Image 2025-01-23 at 6.59.00 PM.jpeg"
            alt="Kikie Kendagor"
            class="w-full h-auto"
          />
        </div>
        <!-- Decorative Ring -->
        <div class="absolute -top-6 -left-6 w-24 h-24 rounded-full border-4 border-purple-900"></div>
        <div class="absolute -bottom-8 -right-8 w-32 h-32 rounded-full border-4 border-gray-300"></div>
      </div>

      <!-- Left Section: Text -->
      <div class="text-center lg:text-left order-2 lg:order-1">
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-purple-900 leading-tight">
          Hi, I am Francisca J. Kipsang.
        </h1>
        <p class="text-lg mt-6 text-gray-700 max-w-2xl mx-auto lg:mx-0">
          A seasoned finance officer with a deep-rooted passion for financial management and accounting. My experience spans across various aspects of finance, from accounting to regulatory compliance, reflecting my commitment to excellence and transparency in financial practices.
        </p>
        <div class="mt-8 flex justify-center lg:justify-start gap-4">
          <!-- Resume Download Button -->
          <button
            @click="downloadCv"
            class="bg-purple-900 text-white px-6 py-3 rounded-lg shadow-lg hover:bg-purple-800 transition cursor-pointer"
          >
            Download My Resume
          </button>
          <!-- Explore My Work Button -->
          <LandingLink
            href="/gallery"
            class="bg-purple-900 text-white border border-purple-900 px-6 py-3 rounded-lg shadow-lg"
          >
            Explore My Work
          </LandingLink>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
/* Optional styles for additional customization */
.cursor-pointer {
  cursor: pointer;
}
</style>