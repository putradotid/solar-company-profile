<template>
  <section class="bg-black text-white py-16">
    <div
      class="max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-8 text-center md:text-left"
    >
      <div v-for="feature in features" :key="feature.title">
        <h3 class="text-xl font-semibold">
          {{ feature.title }}
        </h3>
        <p class="mt-2 text-gray-400">
          {{ feature.description }}
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    title: 'Sustainable Energy',
    description:
      'Power your home with emissions-free, renewable energy directly from the sun.',
  },
  {
    title: 'Tax Incentives',
    description:
      'You may qualify for federal, state and local tax incentives that can reduce installation costs.',
  },
  {
    title: 'Monthly Bill Savings',
    description:
      'Generating energy from the sun helps protect you from rising electricity costs.',
  },
]
</script>
