<template>
  <section class="max-w-6xl mx-auto px-6 py-24">
    <h1 class="text-4xl font-bold mb-10">Proyek Kami</h1>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
      <div
        v-for="project in projects"
        :key="project.title"
        class="group relative overflow-hidden rounded-lg shadow-lg"
      >
        <!-- Image -->
        <img
          :src="project.image"
          :alt="project.title"
          class="h-56 w-full object-cover transition-transform duration-500 group-hover:scale-110"
        />

        <!-- Overlay -->
        <div
          class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition flex flex-col justify-end p-4"
        >
          <h3 class="text-white font-semibold text-lg">
            {{ project.title }}
          </h3>
          <p class="text-gray-300 text-sm">
            {{ project.location }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: 'Solar Panel Rumah Tinggal',
    location: 'Jakarta',
    image:
      'https://images.unsplash.com/photo-1509391366360-2e959784a276?q=80&w=800',
  },
  {
    title: 'Solar Panel Rumah Tinggal',
    location: 'Jakarta',
    image:
      'https://cdn.shopify.com/s/files/1/0011/4102/files/grid-tie-solar-system-components.png?q=80&w=800',
  },
  {
    title: 'Solar Panel Industri',
    location: 'Bekasi',
    image:
      'https://coldwellenergy.com/wp-content/uploads/2023/02/industrial-plant-solar-system.jpg?q=80&w=800',
  },
]
</script>
