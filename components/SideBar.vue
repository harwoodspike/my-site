<template>
  <transition name="none">
    <div
      v-if="isOpen"
      class="w-2/12 bg-gray-100 border-r-2 border-grey-600 p-4 shadow-lg"
    >
      <slot></slot>
    </div>
  </transition>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  props: {
    isOpen: {
      type: Boolean,
      default: false,
    },
  },
});
</script>

<style scoped>
.slide-side-enter-active,
.slide-side-leave-active {
  transition: all 0.9s ease-out;
}
.slide-side-enter,
.slide-side-leave-to {
  transform: translateX(-100%);
}
</style>
