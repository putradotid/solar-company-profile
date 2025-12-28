<template>
  <section class="max-w-6xl mx-auto px-6 py-16">
    <h2 class="text-4xl font-bold">Our Offices</h2>
    <p class="mt-4 text-gray-600 max-w-2xl">
      Varius facilisi mauris sed sit.
    </p>

    <div class="mt-12 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 border-t pt-8">
      <div v-for="office in offices" :key="office.city">
        <h3 class="font-semibold border-l-2 border-blue-500 pl-3">
          {{ office.city }}
        </h3>
        <p class="text-gray-600">{{ office.address }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const offices = [
  { city: 'Los Angeles', address: '4556 Brendan Ferry' },
  { city: 'New York', address: '886 Walter Street' },
  { city: 'Toronto', address: '7363 Cynthia Pass' },
  { city: 'London', address: '114 Cobble Lane' },
]
</script>
