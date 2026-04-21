<script setup>
import { computed } from 'vue'

const props = defineProps({
  title: String,
  description: String,
  link: String,
  linkText: String,
  variant: String,
})

const cardBackgroundVariant = computed(() => {
  return props.variant === 'primary' ? 'bg-gray-100' : 'bg-green-100'
})

const buttonVariantClasses = computed(() => {
  return props.variant === 'primary'
    ? 'bg-black text-white hover:bg-gray-700'
    : 'bg-green-500 text-white hover:bg-green-600'
})
</script>

<template>
  <div class="p-6 rounded-lg shadow-md" :class="cardBackgroundVariant">
    <h2 class="text-2xl font-bold">{{ props.title }}</h2>
    <p class="mt-2 mb-4">{{ props.description }}</p>
    <a :href="props.link" class="inline-block rounded-lg px-4 py-2" :class="buttonVariantClasses">
      {{ props.linkText }}
    </a>
  </div>
</template>
