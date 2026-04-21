<script setup>
import JobListingList from './JobListingList.vue'

defineProps({
  limit: Number,
  showButton: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <section class="bg-green-50 px-4 py-10">
    <div class="container-xl lg:container m-auto">
      <h2 class="text-3xl font-bold text-green-500 mb-6 text-center">Browse Jobs</h2>
      <JobListingList :limit="limit" />
    </div>
  </section>

  <section class="m-auto max-w-lg my-10 px-6" v-if="showButton">
    <a
      href="/jobs"
      class="block bg-black text-white text-center py-4 px-6 rounded-xl hover:bg-gray-700"
    >
      View All Jobs
    </a>
  </section>
</template>
