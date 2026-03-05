<script setup lang="ts">
const testimonials = [
  {
    quote: "IndepHR transformed how we gather and act on employee feedback. The AI insights are incredibly actionable.",
    author: "Sarah van den Berg",
    role: "HR Director",
    company: "TechCorp Netherlands",
  },
  {
    quote: "Finally, a platform where employees feel safe to share honest feedback. Our engagement scores have improved significantly.",
    author: "Mark de Vries",
    role: "People & Culture Manager",
    company: "Innovation Labs",
  },
  {
    quote: "The automated reports save us countless hours. We can now focus on implementing changes instead of analyzing data.",
    author: "Lisa Jansen",
    role: "Chief People Officer",
    company: "GrowthScale BV",
  },
]
</script>

<template>
  <section class="py-20 bg-gradient-to-br from-indep-purple to-indep-violet text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="font-montserrat text-3xl lg:text-4xl font-bold mb-4">
          Trusted by HR Leaders
        </h2>
        <p class="text-xl text-purple-100 max-w-2xl mx-auto">
          See what our customers say about IndepHR
        </p>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div
          v-for="testimonial in testimonials"
          :key="testimonial.author"
          class="bg-white/10 backdrop-blur-sm rounded-xl p-6"
        >
          <svg class="w-10 h-10 text-indep-orange mb-4" fill="currentColor" viewBox="0 0 24 24">
            <path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h3.983v10h-9.983z" />
          </svg>
          <p class="text-lg mb-6">{{ testimonial.quote }}</p>
          <div>
            <p class="font-semibold">{{ testimonial.author }}</p>
            <p class="text-purple-200 text-sm">{{ testimonial.role }}</p>
            <p class="text-purple-300 text-sm">{{ testimonial.company }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
