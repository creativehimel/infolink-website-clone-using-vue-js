<script setup>
import { computed } from 'vue'
import { cva } from 'class-variance-authority'
const props = defineProps({
  RightIcon: {
    type: Object,
    required: false
  },
  intent: {
    type: String,
    validator: (value) =>
      [
        'primary',
        'secondary',
        'danger',
        'info',
        'warning',
        'success',
        'dark',
        'outline-primary',
        'outline-secondary',
        'outline-danger',
        'outline-info',
        'outline-warning',
        'outline-success',
        'outline-dark',
        'link-primary'
      ].includes(value),
    default: 'primary'
  }
})

const buttonClasses = computed(() => {
  return cva('py-2 px-6 rounded font-medium duration-300 flex items-center justify-center', {
    variants: {
      intent: {
        primary: 'bg-indigo-600 hover:bg-indigo-700 text-white',
        secondary: 'bg-gray-500 hover:bg-gray-600 text-white',
        danger: 'bg-red-500 hover:bg-red-600 text-white',
        info: 'bg-teal-500 hover:bg-teal-600 text-white',
        warning: 'bg-yellow-500 hover:bg-yellow-600 text-white',
        success: 'bg-green-500 hover:bg-green-600 text-white',
        dark: 'bg-gray-800 hover:bg-gray-900 text-white',
        'outline-primary':
          'border border-indigo-600 text-indigo-700 hover:bg-indigo-700 hover:text-white',
        'outline-secondary':
          'border border-gray-500 text-gray-500 hover:bg-gray-500 hover:text-white',
        'outline-danger': 'border border-red-500 text-red-500 hover:bg-red-500 hover:text-white',
        'outline-info': 'border border-teal-500 text-teal-500 hover:bg-teal-500 hover:text-white',
        'outline-warning':
          'border border-yellow-500 text-yellow-500 hover:bg-yellow-500 hover:text-white',
        'outline-success':
          'border border-green-500 text-green-500 hover:bg-green-500 hover:text-white',
        'outline-dark': 'border border-gray-800 text-gray-800 hover:bg-gray-800 hover:text-white',
        'link-primary': 'bg-transparent text-indigo-700 hover:text-indigo-800'
      }
    }
  })({
    intent: props.intent
  })
})
</script>

<template>
  <button :class="buttonClasses">
    <slot />
    <component :is="props.RightIcon" class="w-5 h-5 ml-2" />
  </button>
</template>
<style scoped></style>
