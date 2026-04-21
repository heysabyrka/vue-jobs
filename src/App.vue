<script setup>
import AppNavbar from './components/AppNavbar.vue'
import AppHero from './components/AppHero.vue'
import HomeCardList from './components/HomeCardList.vue'
import JobListings from './components/JobListing/JobListings.vue'
</script>

<template>
  <AppNavbar />
  <AppHero />
  <HomeCardList />
  <JobListings :limit="3" :showButton="true" />
</template>
