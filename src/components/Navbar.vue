<script setup lang="ts">
import { ref } from 'vue'
import logo from '../assets/indephr_sm.jpg'

const isMenuOpen = ref(false)

const navLinks = [
  { label: 'Why IndepHR', href: '#why' },
  { label: 'How It Works', href: '#process' },
  { label: 'Pricing', href: '#pricing' },
  { label: 'Team', href: '#team' },
  { label: 'FAQ', href: '#faq' },
  { label: 'Contact', href: '#contact' },
]
</script>

<template>
  <header class="bg-white shadow-sm sticky top-0 z-50">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <a href="/" class="flex items-center">
          <img :src="logo" alt="IndepHR" class="h-10" />
        </a>

        <!-- Desktop nav -->
        <div class="hidden md:flex items-center gap-8">
          <a
            v-for="link in navLinks"
            :key="link.href"
            :href="link.href"
            class="text-gray-600 hover:text-indep-blue transition-colors font-medium"
          >
            {{ link.label }}
          </a>
          <a
            href="#contact"
            class="bg-indep-orange text-white px-5 py-2 rounded-lg font-semibold hover:bg-indep-orange-dark transition-colors"
          >
            Get a Demo
          </a>
        </div>

        <!-- Mobile menu button -->
        <button
          @click="isMenuOpen = !isMenuOpen"
          class="md:hidden p-2"
          aria-label="Toggle menu"
        >
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path
              v-if="!isMenuOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path
              v-else
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>

      <!-- Mobile nav -->
      <div v-if="isMenuOpen" class="md:hidden py-4 border-t">
        <div class="flex flex-col gap-4">
          <a
            v-for="link in navLinks"
            :key="link.href"
            :href="link.href"
            class="text-gray-600 hover:text-indep-blue transition-colors font-medium"
            @click="isMenuOpen = false"
          >
            {{ link.label }}
          </a>
          <a
            href="#contact"
            class="bg-indep-orange text-white px-5 py-2 rounded-lg font-semibold hover:bg-indep-orange-dark transition-colors text-center"
            @click="isMenuOpen = false"
          >
            Get a Demo
          </a>
        </div>
      </div>
    </nav>
  </header>
</template>
