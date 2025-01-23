<script setup>
import { Icon } from '@iconify/vue'; // Ensure this is installed and imported

const certifications = [
  {
    title: "Certified Public Accountant",
    description: "Recognized by The Public Accountants Society for expertise in Public Accounting",
    src: "/CPA CERT.pdf", // Corrected path
    icon: "bx:bxs-badge-check",
  },
  {
    title: "University Degree in Finance",
    description: "Awarded certification for completing University Degree",
    icon: "bx:bxs-tree",
    src: "/UNIVERSITY DEGREE.pdf", // Corrected path
  },
];

const downloadCertification = (certification) => {
  const link = document.createElement('a');
  link.href = certification.src;
  link.download = certification.title + '.pdf'; // Filename for the download
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};
</script>

<template>
  <section class="bg-gray-50 py-16 px-6 lg:px-16">
    <div class="text-center mb-12">
      <h2 class="text-4xl lg:text-5xl font-bold text-purple-900">
        My Certifications
      </h2>
      <p class="text-lg mt-4 text-gray-600 max-w-3xl mx-auto">
        Explore the certifications that demonstrate my expertise in Finance, Accounting, Taxes, and leadership.
      </p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8 lg:gap-10">
      <div
        v-for="certification of certifications"
        :key="certification.title"
        class="bg-white shadow-lg rounded-lg p-4 sm:p-6 lg:p-8 transition-transform transform hover:scale-105 cursor-pointer"
        @click="downloadCertification(certification)"
      >
        <div class="flex items-center mb-4">
          <div class="bg-purple-900 text-white rounded-full p-3 w-12 h-12 flex items-center justify-center">
            <Icon :icon="certification.icon" class="text-2xl" />
          </div>
          <h3 class="ml-4 font-semibold text-lg text-purple-900">
            {{ certification.title }}
          </h3>
        </div>
        <p class="text-gray-600">
          {{ certification.description }}
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.bg-gray-50 {
  background-color: #f9fafb;
}

.text-purple-900 {
  color: #6b21a8;
}

.bg-purple-900 {
  background-color: #6b21a8;
}

.text-gray-600 {
  color: #4b5563;
}

.shadow-lg {
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.transition-transform {
  transition: transform 0.3s ease;
}

.hover\:scale-105:hover {
  transform: scale(1.05);
}

.cursor-pointer {
  cursor: pointer;
}

.rounded-lg {
  border-radius: 0.5rem;
}

.p-4 {
  padding: 1rem;
}

.sm\:p-6 {
  padding: 1.5rem;
}

.lg\:p-8 {
  padding: 2rem;
}

.mb-4 {
  margin-bottom: 1rem;
}

.w-12 {
  width: 3rem;
}

.h-12 {
  height: 3rem;
}

.flex {
  display: flex;
}

.items-center {
  align-items: center;
}

.justify-center {
  justify-content: center;
}

.ml-4 {
  margin-left: 1rem;
}

.font-bold {
  font-weight: 700;
}

.font-semibold {
  font-weight: 600;
}

.text-lg {
  font-size: 1.125rem;
}

.text-2xl {
  font-size: 1.5rem;
}

.text-4xl {
  font-size: 2.25rem;
}

.text-5xl {
  font-size: 3rem;
}

.max-w-3xl {
  max-width: 48rem;
}

.mx-auto {
  margin-left: auto;
  margin-right: auto;
}

.py-16 {
  padding-top: 4rem;
  padding-bottom: 4rem;
}

.px-6 {
  padding-left: 1.5rem;
  padding-right: 1.5rem;
}

.lg\:px-16 {
  padding-left: 4rem;
  padding-right: 4rem;
}

.grid {
  display: grid;
}

.grid-cols-1 {
  grid-template-columns: repeat(1, minmax(0, 1fr));
}

.sm\:grid-cols-2 {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.lg\:grid-cols-3 {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.gap-6 {
  gap: 1.5rem;
}

.sm\:gap-8 {
  gap: 2rem;
}

.lg\:gap-10 {
  gap: 2.5rem;
}

.mt-16 {
  margin-top: 4rem;
}

.mb-12 {
  margin-bottom: 3rem;
}
</style>