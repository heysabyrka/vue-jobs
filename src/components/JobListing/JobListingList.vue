<script setup>
import { ref } from 'vue'
import jobData from '@/jobs.json'
import JobListingItem from './JobListingItem.vue'

defineProps({
  limit: Number,
})

const jobs = ref(jobData)
</script>

<template>
  <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
    <JobListingItem v-for="job in jobs.slice(0, limit || jobs.length)" :key="job.id" v-bind="job" />
  </div>
</template>
