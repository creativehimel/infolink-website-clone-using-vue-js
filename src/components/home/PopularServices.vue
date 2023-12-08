<script setup>
import PopularServiceCard from './PopularServiceCard.vue'
import { StarIcon, RocketLaunchIcon, ComputerDesktopIcon, MapIcon } from '@heroicons/vue/20/solid'
import { HomeInternet, SMEInternet, GPSTracker } from '@/assets/images'

const Services = [
  {
    id: 1,
    img: HomeInternet,
    name: 'Home Internet Connection',
    description: [
      {
        name: '5 Star Service',
        icon: StarIcon
      },
      {
        name: '24/7 Monitoring',
        icon: ComputerDesktopIcon
      },
      {
        name: 'High Speed Internet',
        icon: RocketLaunchIcon
      }
    ]
  },
  {
    id: 2,
    img: SMEInternet,
    name: 'Corporate Internet Connection',
    description: [
      {
        name: '5 Star Service',
        icon: StarIcon
      },
      {
        name: '24/7 Monitoring',
        icon: ComputerDesktopIcon
      },
      {
        name: 'High Speed Internet',
        icon: RocketLaunchIcon
      }
    ]
  },
  {
    id: 3,
    img: GPSTracker,
    name: 'GPS Tracking',
    description: [
      {
        name: '5 Star Service',
        icon: StarIcon
      },
      {
        name: '24/7 Monitoring',
        icon: ComputerDesktopIcon
      },
      {
        name: 'Live Location',
        icon: MapIcon
      }
    ]
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

    <div class="grid grid-cols-3 gap-10 py-10">
      <PopularServiceCard
        v-for="service in Services"
        :key="service.id"
        :title="service.name"
        :description="service.description"
        :image="service.img"
      />
    </div>
  </section>
</template>

<style scoped></style>
