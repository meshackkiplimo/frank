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
    <!-- Header Section -->
    <div class="text-center mb-12">
      <h2 class="text-4xl lg:text-5xl font-extrabold text-purple-900">
        My Certifications
      </h2>
      <p class="text-lg mt-4 text-gray-600 max-w-3xl mx-auto">
        Explore the certifications that demonstrate my expertise in Finance, Accounting, Taxes, and leadership.
      </p>
    </div>

    <!-- Certification Cards -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
      <div
        v-for="certification of certifications"
        :key="certification.title"
        class="bg-white shadow-lg rounded-lg p-6 hover:shadow-2xl transition-shadow transform hover:scale-105 cursor-pointer"
        @click="downloadCertification(certification)"
      >
        <!-- Icon and Title -->
        <div class="flex items-center mb-4">
          <div class="bg-purple-900 text-white rounded-full p-3 w-12 h-12 flex items-center justify-center">
            <Icon :icon="certification.icon" class="text-2xl" />
          </div>
          <h3 class="ml-4 text-lg font-semibold text-purple-900">
            {{ certification.title }}
          </h3>
        </div>

        <!-- Description -->
        <p class="text-gray-600">
          {{ certification.description }}
        </p>
      </div>
    </div>
  </section>
</template>

<!-- No additional custom CSS is necessary because Tailwind handles styling -->
