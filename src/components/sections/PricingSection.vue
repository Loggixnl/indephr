<script setup lang="ts">
const plans = [
  {
    name: 'Starter',
    price: '99',
    description: 'Perfect for small teams getting started with employee feedback',
    features: [
      'Up to 50 employees',
      '4 surveys per year',
      'Basic analytics',
      'Email support',
      'Anonymous responses',
    ],
    highlighted: false,
  },
  {
    name: 'Professional',
    price: '249',
    description: 'For growing organizations that need deeper insights',
    features: [
      'Up to 250 employees',
      'Unlimited surveys',
      'Advanced analytics & AI insights',
      'Priority support',
      'Custom branding',
      'Department comparisons',
      'Action plan generator',
    ],
    highlighted: true,
  },
  {
    name: 'Enterprise',
    price: 'Custom',
    description: 'For large organizations with complex needs',
    features: [
      'Unlimited employees',
      'Unlimited surveys',
      'Full AI-powered insights',
      'Dedicated account manager',
      'SSO integration',
      'API access',
      'Custom integrations',
      'On-site training',
    ],
    highlighted: false,
  },
]
</script>

<template>
  <section id="pricing" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="font-montserrat text-3xl lg:text-4xl font-bold text-indep-blue mb-4">
          Simple, Transparent Pricing
        </h2>
        <p class="text-xl text-gray-600 max-w-2xl mx-auto">
          Choose the plan that fits your organization's needs
        </p>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div
          v-for="plan in plans"
          :key="plan.name"
          :class="[
            'rounded-2xl p-8',
            plan.highlighted
              ? 'bg-gradient-to-br from-indep-blue to-indep-purple text-white shadow-xl scale-105'
              : 'bg-gray-50 text-gray-900',
          ]"
        >
          <h3 class="font-montserrat text-xl font-semibold mb-2">{{ plan.name }}</h3>
          <div class="mb-4">
            <span class="font-montserrat text-4xl font-bold">
              {{ plan.price === 'Custom' ? '' : '€' }}{{ plan.price }}
            </span>
            <span v-if="plan.price !== 'Custom'" :class="plan.highlighted ? 'text-blue-200' : 'text-gray-500'">
              /month
            </span>
          </div>
          <p :class="['mb-6', plan.highlighted ? 'text-blue-100' : 'text-gray-600']">
            {{ plan.description }}
          </p>

          <ul class="space-y-3 mb-8">
            <li
              v-for="feature in plan.features"
              :key="feature"
              class="flex items-start gap-2"
            >
              <svg
                class="w-5 h-5 flex-shrink-0 mt-0.5"
                :class="plan.highlighted ? 'text-indep-orange' : 'text-indep-blue'"
                fill="currentColor"
                viewBox="0 0 20 20"
              >
                <path
                  fill-rule="evenodd"
                  d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                  clip-rule="evenodd"
                />
              </svg>
              <span :class="plan.highlighted ? 'text-white' : 'text-gray-700'">{{ feature }}</span>
            </li>
          </ul>

          <a
            href="#contact"
            :class="[
              'block text-center py-3 px-6 rounded-lg font-semibold transition-colors',
              plan.highlighted
                ? 'bg-indep-orange text-white hover:bg-indep-orange-dark'
                : 'bg-indep-blue text-white hover:bg-indep-blue-dark',
            ]"
          >
            {{ plan.price === 'Custom' ? 'Contact Us' : 'Get Started' }}
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
