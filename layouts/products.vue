<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4 flex justify-between">
        <NuxtLink to="/products" class="font-bold">
          Nuxt Dojo Merch
        </NuxtLink>
        <div class="flex gap-4">
          <NuxtLink to="/products/mens">
            men's clothing
          </NuxtLink>
          <NuxtLink to="/products/womens">
            women's clothing
          </NuxtLink>
          <NuxtLink to="/products/electronics">
            electronics
          </NuxtLink>
          <NuxtLink to="/products/jewelery">
            jewelery
          </NuxtLink>
        </div>
      </nav>
    </header>
    <div class="container mx-auto p-4">
      <slot />
    </div>
    <footer class="container mx-auto p-4 flex justify-between border-t-2">
      <ul class="flex gap-4 ">
        <li>
          <DarkToggle />
        </li>
        <li>
          <NuxtLink to="/">
            Home
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">
            About
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/products">
            Merch
          </NuxtLink>
        </li>
      </ul>
    </footer>
  </div>
</template>

<style scoped>
  .router-link-exact-active {
    color: #12b488;
  }
  a:hover {
    color: #12b488;
  }
</style>
