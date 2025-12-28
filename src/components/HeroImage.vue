<template>
  <section
    class="w-full h-screen bg-cover bg-center"
    :style="`background-image: url('${image}')`"
  ></section>
</template>

<script setup>
defineProps({
  image: {
    type: String,
    required: true,
  },
})
</script>
