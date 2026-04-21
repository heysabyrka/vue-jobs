<script setup>
import CardItem from './HomeCardItem.vue'

const items = [
  {
    title: 'For Developers',
    description: 'Browse our Vue jobs and start your career today',
    link: 'jobs.html',
    linkText: 'Browse Jobs',
    variant: 'primary',
  },
  {
    title: 'For Employers',
    description: 'List your job to find the perfect developer for the role',
    link: 'add-job.html',
    linkText: 'Add Job',
    variant: 'accent',
  },
]
</script>

<template>
  <section class="py-4">
    <div class="container-xl lg:container m-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4 rounded-lg">
        <CardItem v-for="item in items" :key="item.title" v-bind="item" />
      </div>
    </div>
  </section>
</template>
