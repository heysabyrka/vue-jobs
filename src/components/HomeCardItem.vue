<script setup>
import { computed } from 'vue'

const { title, description, link, linkText, variant } = defineProps({
  title: String,
  description: String,
  link: String,
  linkText: String,
  variant: String,
})

const cardBackgroundVariant = computed(() => {
  return variant === 'primary' ? 'bg-gray-100' : 'bg-green-100'
})

const buttonVariantClasses = computed(() => {
  return variant === 'primary'
    ? 'bg-black text-white hover:bg-gray-700'
    : 'bg-green-500 text-white hover:bg-green-600'
})
</script>

<template>
  <div class="p-6 rounded-lg shadow-md" :class="cardBackgroundVariant">
    <h2 class="text-2xl font-bold">{{ title }}</h2>
    <p class="mt-2 mb-4">{{ description }}</p>
    <a :href="link" class="inline-block rounded-lg px-4 py-2" :class="buttonVariantClasses">
      {{ linkText }}
    </a>
  </div>
</template>
