<script setup>
useHead({
  title: 'TM | Tailwindcss crash course',
  meta: [
    { name: 'description', content: 'Traversy Media | Tailwindcss crash course' },
  ],
})

const isOpen = ref(false)

const handlerClick = () => {
  isOpen.value = !isOpen.value
}
</script>

<template>
  <div id="bodypage">
    <nav class="relativ container mx-auto p-6">
      <div class="flex items-center justify-between">
        <!-- logo -->
        <div>
          <img src="img/logo.svg" alt="logo">
        </div>
        <!-- Menu items -->
        <div class="hidden md:flex space-x-4">
          <NuxtLink to="/" class="hover:text-red-500">
            Pricing
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-red-500">
            Product
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-red-500">
            About Us
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-red-500">
            Careers
          </NuxtLink>
          <NuxtLink to="/" class="hover:text-red-500">
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
        <!-- Hamburger Icon -->
        <button
          id="menu-btn"
          class="block hamburger md:hidden focus:outline-none"
          :class="{ open: isOpen }"
          @click="handlerClick"
        >
          <span class="hamburger-top" />
          <span class="hamburger-middle" />
          <span class="hamburger-bottom" />
        </button>
      </div>
      <!-- Mobile Menu -->
      <div class="md:hidden">
        <div
          id="menu"
          :class="{ flex: isOpen }"
          class="absolute flex-col items-center hidden self-end py-8 mt-10 space-y-6 font-bold bg-white sm:w-auto sm:self-center left-6 right-6 drop-shadow-md"
        >
          <a href="#">Pricing</a>
          <a href="#">Product</a>
          <a href="#">About Us</a>
          <a href="#">Careers</a>
          <a href="#">Community</a>
        </div>
      </div>
    </nav>
    <!-- content here -->
    <slot />
  </div>
</template>

<style scoped>
#bodypage {
  background-image: url('img/bg-tablet-pattern.svg');
  background-repeat: no-repeat;
  background-size: 800px;
  background-position: 90% -25%;
}

@media (max-width: 576px) {
  body {
    background-position: 50px -50px;
    background-size: 500px;
  }

}
/* Hamburger Menu */
.hamburger {
  cursor: pointer;
  width: 24px;
  height: 24px;
  transition: all 0.25s;
  position: relative;
}

.hamburger-top,
.hamburger-middle,
.hamburger-bottom {
  position: absolute;
  top: 0;
  left: 0;
  width: 24px;
  height: 2px;
  background: #000;
  transform: rotate(0);
  transition: all 0.5s;
}

.hamburger-middle {
  transform: translateY(7px);
}

.hamburger-bottom {
  transform: translateY(14px);
}

.open {
  transform: rotate(90deg);
  transform: translateY(0px);
}

.open .hamburger-top {
  transform: rotate(45deg) translateY(6px) translate(6px);
}

.open .hamburger-middle {
  display: none;
}

.open .hamburger-bottom {
  transform: rotate(-45deg) translateY(6px) translate(-6px);
}
</style>
