<template>
  <header
    :class="[
      'fixed top-0 w-full z-50 transition-all duration-300',
      isHome ? 'bg-transparent' : 'bg-white shadow'
    ]"
  >
    <nav class="flex items-center justify-between max-w-7xl mx-auto p-6">
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

      <!-- Menu -->
      <ul class="hidden md:flex gap-8 font-semibold">
        <li>
          <router-link
            to="/about"
            :class="linkClass"
          >
            Tentang Kami
          </router-link>
        </li>
        <li>
          <router-link
            to="/services"
            :class="linkClass"
          >
            Layanan
          </router-link>
        </li>
        <li>
          <router-link
            to="/portfolio"
            :class="linkClass"
          >
            Proyek
          </router-link>
        </li>
        <li>
          <router-link
            to="/contact"
            :class="linkClass"
          >
            Kontak
          </router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const isHome = computed(() => route.path === '/')

const linkClass = computed(() =>
  isHome.value
    ? 'text-white hover:underline'
    : 'text-gray-800 hover:text-black'
)
</script>
