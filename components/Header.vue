<template>
  <header class="w-full flex justify-between items-center mx-auto p-2 mb-4 shadow-md  bg-green-600">
    <div class="flex items-center gap-2" text="xl white">
      <NuxtLink class="icon-btn text-3xl" i-carbon-campsite to="/" />
      <NuxtLink to="/" class="font-bold text-white uppercase text-3xl">
        home
      </NuxtLink>
      <DarkToggle />
    </div>

    <nav class="flex gap-4" text="white">
      <NuxtLink to="/" class="font-bold uppercase">
        home
      </NuxtLink>
      <NuxtLink to="/bulma-index" class="font-bold uppercase">
        bulma
      </NuxtLink>
      <NuxtLink to="/" class="font-bold uppercase">
        item-2
      </NuxtLink>
      <NuxtLink to="/old" class="font-bold uppercase">
        old
      </NuxtLink>
    </nav>
  </header>
</template>

<style>
a {
  color: white;
}
</style>
