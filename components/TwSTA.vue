<script setup>

</script>

<template>
  <section id="cta" class="bg-red-400">
    <!-- Flex Container -->
    <div
      class="container flex flex-col items-center justify-between px-6 py-24 mx-auto space-y-12 md:py-12 md:flex-row md:space-y-0"
    >
      <!-- Heading -->
      <h2
        class="text-5xl font-bold text-center text-white md:text-4xl md:max-w-xl md:text-left"
      >
        Simplify how your team works today
      </h2>
      <!-- Button -->
      <div>
        <a
          href="#"
          class="p-3 px-6 pt-2 text-red-400 bg-white rounded-full shadow-2xl hover:bg-gray-900"
        >Get Started</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
#cta {
  background-image: url('img/bg-simplify-section-desktop.svg');
  background-repeat: no-repeat;
}
@media (max-width: 576px) {

  #cta {
    background-image: url('img/bg-simplify-section-mobile.svg');
  }
}
</style>
