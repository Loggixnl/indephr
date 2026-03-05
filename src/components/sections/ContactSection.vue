<script setup lang="ts">
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  company: '',
  employees: '',
  message: '',
})

const isSubmitting = ref(false)
const isSubmitted = ref(false)

const handleSubmit = async () => {
  isSubmitting.value = true
  // Simulate form submission
  await new Promise(resolve => setTimeout(resolve, 1000))
  isSubmitting.value = false
  isSubmitted.value = true
}
</script>

<template>
  <section id="contact" class="py-20 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid lg:grid-cols-2 gap-12">
        <div>
          <h2 class="font-montserrat text-3xl lg:text-4xl font-bold text-indep-blue mb-4">
            Ready to Transform Your Feedback Culture?
          </h2>
          <p class="text-lg text-gray-600 mb-8">
            Get in touch to schedule a demo or discuss how IndepHR can help your organization build a more engaged workforce.
          </p>

          <div class="space-y-6">
            <div class="flex items-start gap-4">
              <div class="w-12 h-12 bg-indep-blue/10 rounded-lg flex items-center justify-center flex-shrink-0">
                <svg class="w-6 h-6 text-indep-blue" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-gray-900">Email Us</h4>
                <a href="mailto:info@indephr.com" class="text-indep-blue hover:underline">info@indephr.com</a>
              </div>
            </div>

            <div class="flex items-start gap-4">
              <div class="w-12 h-12 bg-indep-purple/10 rounded-lg flex items-center justify-center flex-shrink-0">
                <svg class="w-6 h-6 text-indep-purple" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-gray-900">Schedule a Demo</h4>
                <p class="text-gray-600">Book a personalized walkthrough of the platform</p>
              </div>
            </div>

            <div class="flex items-start gap-4">
              <div class="w-12 h-12 bg-indep-orange/10 rounded-lg flex items-center justify-center flex-shrink-0">
                <svg class="w-6 h-6 text-indep-orange" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-gray-900">Quick Start</h4>
                <p class="text-gray-600">Get up and running in less than a day</p>
              </div>
            </div>
          </div>
        </div>

        <div class="bg-white rounded-2xl shadow-lg p-8">
          <div v-if="isSubmitted" class="text-center py-12">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
            </div>
            <h3 class="font-montserrat text-xl font-semibold text-gray-900 mb-2">Thank You!</h3>
            <p class="text-gray-600">We'll be in touch within 24 hours.</p>
          </div>

          <form v-else @submit.prevent="handleSubmit" class="space-y-6">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-700 mb-1">Full Name</label>
              <input
                id="name"
                v-model="form.name"
                type="text"
                required
                class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indep-blue focus:border-transparent outline-none transition-colors"
                placeholder="Your name"
              />
            </div>

            <div>
              <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Work Email</label>
              <input
                id="email"
                v-model="form.email"
                type="email"
                required
                class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indep-blue focus:border-transparent outline-none transition-colors"
                placeholder="you@company.com"
              />
            </div>

            <div>
              <label for="company" class="block text-sm font-medium text-gray-700 mb-1">Company Name</label>
              <input
                id="company"
                v-model="form.company"
                type="text"
                required
                class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indep-blue focus:border-transparent outline-none transition-colors"
                placeholder="Your company"
              />
            </div>

            <div>
              <label for="employees" class="block text-sm font-medium text-gray-700 mb-1">Number of Employees</label>
              <select
                id="employees"
                v-model="form.employees"
                required
                class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indep-blue focus:border-transparent outline-none transition-colors"
              >
                <option value="">Select...</option>
                <option value="1-50">1-50</option>
                <option value="51-250">51-250</option>
                <option value="251-1000">251-1000</option>
                <option value="1000+">1000+</option>
              </select>
            </div>

            <div>
              <label for="message" class="block text-sm font-medium text-gray-700 mb-1">Message (Optional)</label>
              <textarea
                id="message"
                v-model="form.message"
                rows="3"
                class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indep-blue focus:border-transparent outline-none transition-colors resize-none"
                placeholder="Tell us about your needs..."
              ></textarea>
            </div>

            <button
              type="submit"
              :disabled="isSubmitting"
              class="w-full bg-indep-orange text-white py-3 px-6 rounded-lg font-semibold hover:bg-indep-orange-dark transition-colors disabled:opacity-50 disabled:cursor-not-allowed"
            >
              {{ isSubmitting ? 'Sending...' : 'Request a Demo' }}
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>
