<template>
  <div class="flex flex-col h-full">
    <Header />
    <main class="container mx-auto grow">
      <slot />
    </main>
    <MyFooter />
  </div>
</template>

