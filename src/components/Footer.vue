<script setup lang="ts">
const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="bg-indep-blue text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
      <div class="grid md:grid-cols-4 gap-8">
        <div class="md:col-span-2">
          <span class="font-montserrat font-bold text-2xl">IndepHR</span>
          <p class="mt-2 text-blue-200 italic">Honest voices. Stronger organisations.</p>
          <p class="mt-4 text-blue-100 max-w-md">
            AI-assisted feedback platform helping HR professionals truly listen to their people and act on insights.
          </p>
        </div>

        <div>
          <h4 class="font-montserrat font-semibold mb-4">Quick Links</h4>
          <ul class="space-y-2 text-blue-100">
            <li><a href="#why" class="hover:text-white transition-colors">Why IndepHR</a></li>
            <li><a href="#process" class="hover:text-white transition-colors">How It Works</a></li>
            <li><a href="#pricing" class="hover:text-white transition-colors">Pricing</a></li>
            <li><a href="#faq" class="hover:text-white transition-colors">FAQ</a></li>
          </ul>
        </div>

        <div>
          <h4 class="font-montserrat font-semibold mb-4">Contact</h4>
          <ul class="space-y-2 text-blue-100">
            <li><a href="#contact" class="hover:text-white transition-colors">Get in Touch</a></li>
            <li><a href="mailto:info@indephr.com" class="hover:text-white transition-colors">info@indephr.com</a></li>
          </ul>
        </div>
      </div>

      <div class="border-t border-blue-400 mt-8 pt-8 text-center text-blue-200">
        <p>&copy; {{ currentYear }} IndepHR. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>
