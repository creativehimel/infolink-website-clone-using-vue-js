<script setup>
import Button from '../Button.vue'
</script>

<template>
  <section class="container mx-auto grid grid-cols-2 py-16 items-center px-[80px]">
    <div class="grid-col-1 py-10 space-y-6">
      <p class="font-nunito font-[500] text-sm py-1.5 px-6 border-2 rounded-full inline-block">
        Get <span class="text-indigo-600">connected</span> with InfoLink Internet.
      </p>
      <h1 class="text-4xl font-nunito font-[700] tracking-wider leading-tight">
        We are best For <br />
        Internet Service
      </h1>
      <p class="mt-5 text-lg font-nunito font-[500]">
        To get started with us, please go over all of our internet plans and other plans to let our
        operators know which one works for you the best! We guarantee high-quality customer support
        service with high-speed FTTH broadband connection all over the country.
      </p>
      <Button intent="outline-primary">CallBack Request</Button>
    </div>
    <div>
      <img class="max-w-[80%] rounded mx-auto" alt="Infolink" src="@/assets/images/safa1.png" />
    </div>
  </section>
</template>
<style scoped></style>
