<script setup>
const props = defineProps({
  title: String,
  description: Array,
  image: String
})
import Button from '../Button.vue'
import { ChevronRightIcon } from '@heroicons/vue/20/solid'
</script>
<template>
  <section class="bg-white space-y-6 max-w-sm w-full mx-auto rounded-md shadow">
    <div>
      <img class="w-full rounded-t-md" :src="props.image" alt="" />
    </div>
    <div class="space-y-4 px-6">
      <h1 class="text-xl font-nunito font-[600]">
        {{ props.title }}
      </h1>
      <ul>
        <li
          v-for="item in props.description"
          :key="item.name"
          class="flex items-center text-gray-700 text-md"
        >
          <component :is="item.icon" class="w-5 h-5 mr-2" />
          {{ item.name }}
        </li>
      </ul>
    </div>
    <div>
      <Button :intent="'primary'" :RightIcon="ChevronRightIcon" class="w-full">See More</Button>
    </div>
  </section>
</template>

<style scoped></style>
