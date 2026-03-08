<script setup lang="ts">
import procesImage from '../../assets/indephr_process.svg'
</script>

<template>
  <section class="bg-gradient-to-br from-indep-blue to-indep-purple text-white py-20 lg:py-32">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <div>
          <p class="text-indep-orange font-semibold mb-4">Honest voices. Stronger organisations.</p>
          <h1 class="font-montserrat text-4xl lg:text-5xl font-bold leading-tight mb-6">
            Transform Employee Feedback Into Meaningful Change
          </h1>
          <p class="text-xl text-blue-100 mb-8 max-w-lg">
            IndepHR is an AI-assisted feedback platform that helps HR professionals truly listen to their people and act on their insights.
          </p>
          <div class="flex flex-wrap gap-4">
            <a
              href="#contact"
              class="bg-indep-orange text-white px-8 py-3 rounded-lg font-semibold hover:bg-indep-orange-dark transition-colors"
            >
              Request a Demo
            </a>
            <a
              href="#process"
              class="border-2 border-white text-white px-8 py-3 rounded-lg font-semibold hover:bg-white hover:text-indep-blue transition-colors"
            >
              Learn More
            </a>
          </div>
        </div>
        <div class="hidden lg:flex justify-center">
          <img :src="procesImage" alt="IndepHR Feedback Process" class="max-w-full h-auto" />
        </div>
      </div>
    </div>
  </section>
</template>
