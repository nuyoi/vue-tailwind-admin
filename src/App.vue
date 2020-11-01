<template>
  <div id="app" class="flex h-screen bg-gray-50 dark:bg-gray-900">
    <!-- SideBar -->
    <aside
      class="hidden w-64 overflow-y-auto bg-white dark:bg-gray-800 md:block flex-shrink-0 py-4"
    >
      <span
        href="#"
        class="ml-6 text-lg font-bold text-gray-800 dark:text-gray-200"
      >
        BESIGN
      </span>
      <ul class="mt-6">
        <router-link
          to="/"
          class="inline-flex items-center w-full text-sm font-semibold text-gray-800 transition-colors duration-150 hover:text-gray-800 dark:hover:text-gray-200 dark:text-gray-100 px-6 py-3"
        >
          <i class="fas fa-chart-pie"></i>
          <span class="ml-4">대시보드</span>
        </router-link>
        <li class="relative px-6 py-3" @mouseup="mouseOver2">
          <router-link
            to="/about"
            class="inline-flex items-center w-full text-sm font-semibold text-gray-800 transition-colors duration-150 hover:text-gray-800 dark:hover:text-gray-200 dark:text-gray-100"
          >
            <span
              v-show="active2"
              class="absolute inset-y-0 left-0 w-1 bg-purple-600"
            ></span>
            <span v-html="icon"></span>
            <span class="ml-4">유저관리</span>
          </router-link>
        </li>
      </ul>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </aside>

    <!-- Main Content -->
    <div class="flex flex-col flex-1 w-full">
      <header class="z-10 py-4 bg-white shadow-md dark:bg-gray-800">
        <div
          class="container flex items-center justify-between h-full px-6 mx-auto text-purple-600 dark:text-purple-300"
        ></div>
      </header>

      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active1: false,
      active2: false,
      icon:
        '<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5.121 17.804A13.937 13.937 0 0112 16c2.5 0 4.847.655 6.879 1.804M15 10a3 3 0 11-6 0 3 3 0 016 0zm6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>',
      items: [
        // {
        //   icon:
        // }
      ]
    };
  },
  methods: {
    mouseOver1() {
      this.active1 = true;
    },
    mouseOver2() {
      this.active2 = !this.active2;
    }
  }
};
</script>
<style>
.router-link-exact-active {
  @apply bg-blue-500;
  @apply text-white;
}
</style>

<style src="./assets/tailwind.css" />
