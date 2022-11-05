<script setup>
useHead({
  title: 'TM | Tailwindcss crash course',
  meta: [
    { name: 'description', content: 'Traversy Media | Tailwindcss crash course' },
  ],
})
</script>

<template>
  <div>
    <nav class="relativ container mx-auto p-6">
      <div class="flex items-center justify-between">
        <!-- logo -->
        <div>
          <img src="img/logo.svg" alt="logo">
        </div>
        <!-- Menu items -->
        <div class="hidden md:flex space-x-4">
          <NuxtLink to="/" class="hover:text-cool-gray-500">
            Pricing
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-cool-gray-500">
            Product
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-cool-gray-500">
            About Us
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-cool-gray-500">
            Careers
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-cool-gray-500">
            Community
          </NuxtLink>
        </div>

        <!-- Button -->
        <NuxtLink
          to="/"
          class="hidden md:block text-white p-3 px-6 rounded-full bg-red-400 hover:bg-red-300"
        >
          Get Started
        </NuxtLink>
      </div>
    </nav>
    <!-- content here -->
    <slot />
  </div>
</template>

<style scoped>
  .router-link-exact-active {
    color: #12b488;
  }
</style>
