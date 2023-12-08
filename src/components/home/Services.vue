<script setup>
import ServiceCard from './ServiceCard.vue'
import {
  HomeIcon,
  BuildingOfficeIcon,
  BuildingStorefrontIcon,
  ServerStackIcon,
  MapIcon,
  WindowIcon,
  EnvelopeIcon,
  CloudIcon
} from '@heroicons/vue/20/solid'

const Services = [
  {
    id: 1,
    icon: HomeIcon,
    name: 'Home Internet',
    description: 'Get ready for more potential and more opportunity'
  },
  {
    id: 2,
    icon: BuildingOfficeIcon,
    name: 'Corporate Connectivity',
    description: 'More than 1K corporate clients have trust in us'
  },
  {
    id: 3,
    icon: BuildingStorefrontIcon,
    name: 'SME Internet',
    description: 'Designed for more speed within a reasonable price'
  },
  {
    id: 4,
    icon: ServerStackIcon,
    name: 'Dedicated Server',
    description: 'Powerful Dedicated SSD Hosting with Root Access'
  },
  {
    id: 5,
    icon: MapIcon,
    name: 'GPS Tracking',
    description: 'Suitable for personal use or any type of business'
  },
  {
    id: 6,
    icon: WindowIcon,
    name: 'Website Development',
    description: 'You deserve a beautiful, easy website'
  },
  {
    id: 7,
    icon: EnvelopeIcon,
    name: 'Business Email',
    description: 'The most well-known which is said to have originated'
  },
  {
    id: 8,
    icon: CloudIcon,
    name: 'Web Hosting',
    description: 'Build your ideal website with our easy-to-use Hosting'
  }
]
</script>
<template>
  <section class="container mx-auto px-[80px]">
    <div class="text-center py-10 space-y-4">
      <h1 class="text-3xl text-center font-nunito font-[700] tracking-wider leading-tight">
        Explore Popular Services
      </h1>
      <p class="text-lg text-center font-nunito font-[500]">
        Get connected with <span class="text-indigo-600"> InfoLink Limited </span> that can provide
        your every technology need <br />
        to connect the world.
      </p>
    </div>

    <div class="grid grid-cols-4 gap-10 py-10">
      <ServiceCard
        v-for="service in Services"
        :key="service.id"
        :title="service.name"
        :description="service.description"
        :icon="service.icon"
      />
    </div>
  </section>
</template>

<style scoped></style>
