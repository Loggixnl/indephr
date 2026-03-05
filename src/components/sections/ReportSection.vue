<template>
  <section class="py-20 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <div>
          <h2 class="font-montserrat text-3xl lg:text-4xl font-bold text-indep-blue mb-6">
            Clear, Actionable Reports
          </h2>
          <p class="text-lg text-gray-600 mb-6">
            Our visual reports transform complex feedback data into clear insights that anyone can understand and act upon.
          </p>

          <ul class="space-y-4">
            <li class="flex items-start gap-3">
              <svg class="w-6 h-6 text-indep-orange flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Interactive dashboards with real-time data</span>
            </li>
            <li class="flex items-start gap-3">
              <svg class="w-6 h-6 text-indep-orange flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Sentiment analysis and trend identification</span>
            </li>
            <li class="flex items-start gap-3">
              <svg class="w-6 h-6 text-indep-orange flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Department and team comparisons</span>
            </li>
            <li class="flex items-start gap-3">
              <svg class="w-6 h-6 text-indep-orange flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">AI-generated executive summaries</span>
            </li>
            <li class="flex items-start gap-3">
              <svg class="w-6 h-6 text-indep-orange flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Export to PDF for stakeholder presentations</span>
            </li>
          </ul>
        </div>

        <div class="bg-white rounded-2xl shadow-lg p-6">
          <div class="flex justify-between items-center mb-6">
            <h4 class="font-montserrat font-semibold text-gray-900">Engagement Overview</h4>
            <span class="text-sm text-gray-500">Q4 2024</span>
          </div>

          <!-- Mock chart -->
          <div class="space-y-4">
            <div>
              <div class="flex justify-between text-sm mb-1">
                <span class="text-gray-600">Overall Satisfaction</span>
                <span class="font-semibold text-indep-blue">78%</span>
              </div>
              <div class="h-3 bg-gray-100 rounded-full overflow-hidden">
                <div class="h-full bg-indep-blue rounded-full" style="width: 78%"></div>
              </div>
            </div>

            <div>
              <div class="flex justify-between text-sm mb-1">
                <span class="text-gray-600">Work-Life Balance</span>
                <span class="font-semibold text-indep-purple">65%</span>
              </div>
              <div class="h-3 bg-gray-100 rounded-full overflow-hidden">
                <div class="h-full bg-indep-purple rounded-full" style="width: 65%"></div>
              </div>
            </div>

            <div>
              <div class="flex justify-between text-sm mb-1">
                <span class="text-gray-600">Career Growth</span>
                <span class="font-semibold text-indep-violet">72%</span>
              </div>
              <div class="h-3 bg-gray-100 rounded-full overflow-hidden">
                <div class="h-full bg-indep-violet rounded-full" style="width: 72%"></div>
              </div>
            </div>

            <div>
              <div class="flex justify-between text-sm mb-1">
                <span class="text-gray-600">Management Trust</span>
                <span class="font-semibold text-indep-orange">84%</span>
              </div>
              <div class="h-3 bg-gray-100 rounded-full overflow-hidden">
                <div class="h-full bg-indep-orange rounded-full" style="width: 84%"></div>
              </div>
            </div>
          </div>

          <div class="mt-6 pt-6 border-t">
            <div class="flex items-center gap-2 text-sm text-gray-500">
              <svg class="w-4 h-4 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M12 7a1 1 0 110-2h5a1 1 0 011 1v5a1 1 0 11-2 0V8.414l-4.293 4.293a1 1 0 01-1.414 0L8 10.414l-4.293 4.293a1 1 0 01-1.414-1.414l5-5a1 1 0 011.414 0L11 10.586 14.586 7H12z" clip-rule="evenodd" />
              </svg>
              <span>+12% improvement from last quarter</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
