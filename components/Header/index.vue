<template>
  <header
    class="flex items-center justify-between md:justify-center fixed w-screen inset-x-0 top-0 p-3 md:px-20 lg:px-28 md:h-20 z-50"
  >
    <NuxtImg src="/logo.webp" sizes="40px md:50px lg:60px" />

    <HeaderNavbar :isMenuMobileOpened="isMenuMobileOpened" />
    <button>
      <span></span>
    </button>
    <!-- <UIcon
      :name="`i-material-symbols:${isMenuMobileOpened ? 'close' : 'menu'}`"
      class="cursor-pointer z-50 md:!hidden"
      width="40"
      height="40"
      dynamic
      @click="handleMenuMobile"
    /> -->
  </header>
</template>

<script lang="ts" setup>
let isMenuMobileOpened = ref(false);

function handleMenuMobile() {
  isMenuMobileOpened.value = !isMenuMobileOpened.value;
}
</script>

<style></style>
