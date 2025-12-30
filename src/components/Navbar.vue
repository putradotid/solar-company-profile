<template>
  <!-- HEADER FULL WIDTH -->
  <header
    :class="[
      'fixed top-0 left-0 w-full z-50 transition-all duration-300',
      isHome ? 'bg-transparent' : 'bg-white shadow'
    ]"
  >
    <!-- NAVBAR MOBILE: FULL WIDTH -->
    <div class="flex items-center justify-between px-4 py-4 md:hidden">
      <!-- Logo -->
      <router-link
        to="/"
        :class="[
          'font-bold text-lg',
          isHome ? 'text-white' : 'text-gray-900'
        ]"
      >
        Solar Panel
      </router-link>

      <!-- Hamburger -->
      <button @click="open = !open" aria-label="Toggle menu">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          :class="isHome ? 'text-white' : 'text-gray-900'"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
    </div>

    <!-- NAVBAR DESKTOP: CENTERED -->
    <div class="hidden md:flex items-center justify-between max-w-7xl mx-auto px-6 py-6">
      <router-link
        to="/"
        :class="[
          'font-bold text-lg',
          isHome ? 'text-white' : 'text-gray-900'
        ]"
      >
        Solar Panel
      </router-link>

      <ul class="flex gap-8 font-semibold">
        <li v-for="item in menus" :key="item.path">
          <router-link
            :to="item.path"
            :class="linkClass"
          >
            {{ item.label }}
          </router-link>
        </li>
      </ul>
    </div>

    <!-- MOBILE MENU DROPDOWN -->
    <div
      v-if="open"
      class="md:hidden bg-white shadow-lg"
    >
      <ul class="flex flex-col divide-y">
        <li v-for="item in menus" :key="item.path">
          <router-link
            :to="item.path"
            class="block px-4 py-4 text-gray-800 font-semibold"
            @click="open = false"
          >
            {{ item.label }}
          </router-link>
        </li>
      </ul>
    </div>
  </header>
</template>

<script setup>
import { ref, computed, watch } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const open = ref(false)

const isHome = computed(() => route.path === '/')

const linkClass = computed(() =>
  isHome.value
    ? 'text-white hover:underline'
    : 'text-gray-800 hover:text-black'
)

const menus = [
  { label: 'Tentang Kami', path: '/about' },
  { label: 'Layanan', path: '/services' },
  { label: 'Proyek', path: '/portfolio' },
  { label: 'Kontak', path: '/contact' },
]

watch(
  () => route.path,
  () => (open.value = false)
)
</script>
