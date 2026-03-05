<script setup lang="ts">
const team = [
  {
    name: 'Team Member 1',
    role: 'Co-Founder & CEO',
    bio: 'Passionate about transforming workplace culture through honest feedback.',
  },
  {
    name: 'Team Member 2',
    role: 'Co-Founder & CTO',
    bio: 'Building AI-powered solutions that make a real difference for HR professionals.',
  },
  {
    name: 'Team Member 3',
    role: 'Head of Product',
    bio: 'Focused on creating intuitive experiences that empower organizations.',
  },
]
</script>

<template>
  <section id="team" class="py-20 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="font-montserrat text-3xl lg:text-4xl font-bold text-indep-blue mb-4">
          Meet Our Team
        </h2>
        <p class="text-xl text-gray-600 max-w-2xl mx-auto">
          Dedicated professionals building the future of employee engagement
        </p>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div
          v-for="member in team"
          :key="member.name"
          class="bg-white rounded-xl p-6 text-center shadow-sm hover:shadow-md transition-shadow"
        >
          <div class="w-24 h-24 bg-gradient-to-br from-indep-blue to-indep-purple rounded-full mx-auto mb-4 flex items-center justify-center">
            <svg class="w-12 h-12 text-white" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z" />
            </svg>
          </div>
          <h3 class="font-montserrat text-xl font-semibold text-gray-900 mb-1">{{ member.name }}</h3>
          <p class="text-indep-purple font-medium mb-3">{{ member.role }}</p>
          <p class="text-gray-600">{{ member.bio }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
