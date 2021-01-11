<template>
  <div class="flex flex-wrap bg-white w-full h-screen">
    <SideBar :is-open="sideBarOpen">
      <div class="flex flex-col">
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/projects">Projects</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/contact">Contact</NuxtLink>
      </div>
    </SideBar>
    <div :class="[{ 'w-10/12': sideBarOpen, 'w-full': !sideBarOpen }]">
      <div
        :class="['fixed', 'p-4', { open: sideBarOpen }]"
        @click="toggleSideBar"
      >
        <font-awesome-icon class="text-lg" :icon="['fas', 'bars']" />
      </div>
      <div class="h-screen flex justify-center items-center">
        <Nuxt />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    sideBarOpen: false,
  }),
  methods: {
    toggleSideBar() {
      this.sideBarOpen = !this.sideBarOpen;
    },
  },
};
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
