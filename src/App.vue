<template>
  <div id="app" class="flex h-screen bg-gray-50 dark:bg-gray-900">
    <!-- SideBar -->
    <aside
      class="hidden w-64 overflow-y-auto bg-white dark:bg-gray-800 md:block flex-shrink-0"
    >
      <ul class="mt-6">
        <li class="relative px-6 py-3">
          <router-link
            to="/"
            class="inline-flex items-center w-full text-sm font-semibold text-gray-800 transition-colors duration-150 hover:text-gray-800 dark:hover:text-gray-200 dark:text-gray-100"
          >
            <span
              class="absolute inset-y-0 left-0 w-1 bg-purple-600"
              aria-hidden="true"
            ></span>
            <svg
              class="w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M11 3.055A9.001 9.001 0 1020.945 13H11V3.055z"
              ></path>
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M20.488 9H15V3.512A9.025 9.025 0 0120.488 9z"
              ></path>
            </svg>
            <span class="ml-4">대시보드</span>
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

<style src="./assets/tailwind.css" />
