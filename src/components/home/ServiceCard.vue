<script setup>
const props = defineProps({
  title: String,
  description: Array,
  icon: Object
})
import Button from '../Button.vue'
import { ChevronRightIcon } from '@heroicons/vue/20/solid'
</script>
<template>
  <section class="bg-white space-y-6 max-w-sm w-full mx-auto rounded-md shadow hover:shadow-md">
    <div class="space-y-4 px-3 pt-12 pb-6">
      <component :is="props.icon" class="w-14 h-14 mx-auto text-indigo-500" />
      <h3 class="text-xl font-nunito font-[600] text-center text-gray-600">{{ props.title }}</h3>
      <p class="text-md font-nunito font-[500] text-center text-gray-500">
        {{ props.description }}
      </p>
      <Button
        intent="'link-primary'"
        :RightIcon="ChevronRightIcon"
        class="w-full text-indigo-600 hover:text-indigo-700"
        >Read More</Button
      >
    </div>
  </section>
</template>

<style scoped></style>
