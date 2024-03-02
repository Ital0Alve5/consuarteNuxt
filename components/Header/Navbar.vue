<template>
  <nav
    class="absolute shadow-xl md:shadow-none md:static mx-2 md:mx-0 top-full md:h-full md:w-full md:max-w-[940px] transition-transform origin-top md:scale-100 inset-x-0"
    :class="[isMenuMobileOpened ? 'scale-y-100' : 'scale-y-0']"
  >
    <ul
      class="md:w-full p-3 md:p-0 bg-red-800 rounded-bl-xl rounded-br-xl md:bg-transparent md:flex md:justify-center md:items-center"
    >
      <li v-for="item in menuItems">
        <NuxtLink
          to="#"
          class="w-full inline-block px-5 py-3 hover:bg-red-200 hover:text-black"
        >
          {{ item }}
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script lang="ts" setup>
defineProps({
  isMenuMobileOpened: {
    type: Boolean,
    default: false,
  },
});

const menuItems = ["Home", "Work", "Contact", "News"];
</script>

<style></style>
