<script setup lang="ts">
import { ref } from 'vue'

const faqs = [
  {
    question: 'How does IndepHR ensure anonymity?',
    answer: 'IndepHR uses advanced encryption and data separation techniques to guarantee that individual responses can never be traced back to specific employees. We never store identifying information alongside feedback data, and our system is designed from the ground up with privacy as a core principle.',
  },
  {
    question: 'What kind of surveys can I create?',
    answer: 'You can create various types of surveys including engagement surveys, pulse checks, 360-degree feedback, onboarding surveys, exit interviews, and custom surveys. Our AI assistant helps you craft effective questions tailored to your specific needs.',
  },
  {
    question: 'How does the AI-powered analysis work?',
    answer: 'Our AI analyzes open-text responses to identify themes, sentiment, and actionable insights. It processes feedback to surface patterns you might miss, generates executive summaries, and provides strategic recommendations for improvement.',
  },
  {
    question: 'Can I integrate IndepHR with our existing HR systems?',
    answer: 'Yes, IndepHR offers integrations with popular HRIS platforms, communication tools like Slack and Microsoft Teams, and provides API access for custom integrations. Enterprise plans include dedicated support for complex integration needs.',
  },
  {
    question: 'What support do you offer?',
    answer: 'All plans include email support. Professional plans get priority support with faster response times. Enterprise customers receive a dedicated account manager, on-site training, and 24/7 support options.',
  },
  {
    question: 'Is there a minimum contract period?',
    answer: 'Our Starter and Professional plans are available on monthly or annual billing (with a discount for annual). Enterprise contracts are customized based on your organization\'s needs.',
  },
]

const openIndex = ref<number | null>(null)

const toggle = (index: number) => {
  openIndex.value = openIndex.value === index ? null : index
}
</script>

<template>
  <section id="faq" class="py-20 bg-white">
    <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="font-montserrat text-3xl lg:text-4xl font-bold text-indep-blue mb-4">
          Frequently Asked Questions
        </h2>
        <p class="text-xl text-gray-600">
          Everything you need to know about IndepHR
        </p>
      </div>

      <div class="space-y-4">
        <div
          v-for="(faq, index) in faqs"
          :key="index"
          class="border border-gray-200 rounded-lg overflow-hidden"
        >
          <button
            @click="toggle(index)"
            class="w-full px-6 py-4 text-left flex justify-between items-center hover:bg-gray-50 transition-colors"
          >
            <span class="font-semibold text-gray-900">{{ faq.question }}</span>
            <svg
              class="w-5 h-5 text-gray-500 transition-transform"
              :class="{ 'rotate-180': openIndex === index }"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div
            v-if="openIndex === index"
            class="px-6 pb-4 text-gray-600"
          >
            {{ faq.answer }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
