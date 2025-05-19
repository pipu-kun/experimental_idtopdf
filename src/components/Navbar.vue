<script setup>
  import { AiOutlineSearch } from "vue-icons-plus/ai";
</script>

<template>
  <nav class="navbar fixed top-0 left-0 w-full px-4 py-2 shadow-sm bg-white dark:bg-[#1a1a1a] text-black dark:text-white z-50">
    <div class="max-w-7xl mx-auto flex items-center justify-between">
      <img src="/vite.svg">
      <div class="button-default w-full mx-5 flex">
        <AiOutlineSearch class="pl-1"/> <p class="pl-1">Search Tools</p>
      </div>
      <div @click="showMenu = !showMenu" class="flex">
          <button type="button"
              class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400 dark:text-gray-400 dark:hover:text-gray-200">
              <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                  <path fill-rule="evenodd"
                      d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z">
                  </path>
              </svg>
          </button>
      </div>
    </div>
    <div :class="['mt-4 space-y-2', showMenu ? 'flex flex-col' : 'hidden']">
      <router-link to="/" class="p-2 rounded-md hover:bg-zinc-200 dark:hover:bg-zinc-800">Home</router-link>
      <router-link to="/about" class="p-2 rounded-md hover:bg-zinc-200 dark:hover:bg-zinc-800">About</router-link>
    </div>
  </nav>
</template>

<script>
  export default {
    data() {
      return {
        showMenu: false
      }
    }
  }
</script>
