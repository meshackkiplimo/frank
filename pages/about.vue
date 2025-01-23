<script setup>
definePageMeta({
  layout: "landing",
});
</script>

<template>
  <section class="py-16 bg-gray-50" id="about-me">
    <div class="max-w-7xl mx-auto px-6 lg:px-12 text-center lg:text-left">
      <h2 class="text-4xl font-extrabold text-purple-900 mb-10">About Me</h2>
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Image Section -->
        <div class="flex justify-center">
          <img
            src="/assets/img/WhatsApp Image 2025-01-23 at 6.59.00 PM.jpeg"
            alt="Wildlife Biologist"
            class="rounded-full w-56 h-56 object-cover shadow-2xl transition-transform transform hover:scale-105"
          />
        </div>

        <!-- Text Section -->
        <div>
          <p class="text-lg text-gray-800 leading-relaxed mb-6">
  Hi, I’m <span class="font-semibold text-purple-800">Kipsang Jepngetich Francisca</span>, a meticulous finance officer with a profound passion for financial stewardship and regulatory compliance. My career, spanning over several years, has been dedicated to the nuanced world of financial accounting, tax strategy, and asset management, all aimed at promoting transparency and excellence in financial practices.
</p>
<p class="text-lg text-gray-800 leading-relaxed mb-6">
  I specialize in <strong>financial analysis</strong>, providing insights that guide organizational decision-making. My expertise includes crafting detailed financial forecasts, managing budgets, and ensuring that all financial reporting adheres to the highest standards of accuracy and compliance. I've worked alongside various organizations, from government bodies to private entities, to enhance their financial health and operational efficiency.
</p>
<p class="text-lg text-gray-800 leading-relaxed mb-6">
  My approach merges <strong>traditional accounting</strong> with <strong>modern financial technologies</strong>, ensuring that my work not only meets current standards but also anticipates future trends. I'm committed to continuous professional development, as evidenced by my ongoing pursuit of CPA certification and advanced tax education. My goal is to leverage my skills in a role where I can contribute to world-class financial management, driving both growth and sustainability.
</p>
          <div class="mt-8">
            <a
              href="/contact"
              class="inline-block px-8 py-4 bg-purple-600 text-white text-lg font-semibold rounded-lg shadow-md hover:bg-purple-700 transform transition-all duration-300 hover:-translate-y-1"
            >
              Get in Touch
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutMe",
};
</script>

<style scoped>
/* Custom hover effect for smoother transitions */
img:hover {
  box-shadow: 0 8px 24px rgba(0, 128, 0, 0.2);
}
</style>
