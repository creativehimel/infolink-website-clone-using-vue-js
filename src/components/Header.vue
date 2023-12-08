<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <header class="bg-white shadow-sm py-3 px-[120px]">
    <nav class="container mx-auto flex justify-between items-center">
      <img
        alt="Vue logo"
        class="logo"
        src="../assets/images/logo-dark.png"
        width="125"
        height="125"
      />
      <ul class="flex items-center text-md gap-3 font-nunito font-[600]">
        <li>
          <RouterLink to="/">HOME INTERNET</RouterLink>
        </li>
        <li>
          <RouterLink to="/">BUSINESS SOLUTION</RouterLink>
        </li>
        <li>
          <RouterLink to="/">FTP</RouterLink>
        </li>
        <li>
          <RouterLink to="/">TRACKER</RouterLink>
        </li>
      </ul>
      <div class="flex items-center gap-3 font-nunito font-[600]">
        <RouterLink
          to="/sign-up"
          class="bg-red-600 hover:bg-red-700 text-white px-7 py-2.5 rounded duration-300"
          >Sign Up</RouterLink
        >
        <RouterLink
          to="/pay-now"
          class="bg-blue-600 hover:bg-blue-700 text-white px-7 py-2.5 rounded duration-300"
          >Pay Now</RouterLink
        >
        <RouterLink
          to="/login"
          class="bg-blue-600 hover:bg-blue-700 text-white px-7 py-2.5 rounded duration-300"
          >Login</RouterLink
        >
      </div>
    </nav>
  </header>
</template>
<style scoped></style>
