<template>
  <div id="app" class="flex flex-wrap">
    <!-- SideBar -->
    <div id="nav" class="w-1/5 bg-gray-900 h-screen">
      <ul class="list-reset flex flex-col text-gray-400">
        <li class="pl-3">
          <router-link to="/">
            <i class="fas fa-chart-pie"></i>
            <span class="pl-3 inline-block align-middle">대시보드</span>
          </router-link>
        </li>
      </ul>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>

    <!-- Main Content -->
    <div class="w-4/5 bg-gray-100">
      <router-view />
    </div>
  </div>
</template>

<style src="./assets/tailwind.css" />
