<script setup>

</script>

<template>
  <div class="page-grid">
    <BulmaBNavbar />
    <main>
      <slot />
    </main>
    <BulmaBFooter />
  </div>
</template>

<style  scoped>
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css";

.page-grid {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
.page-grid main {
  flex-grow: 1;
}
</style>
