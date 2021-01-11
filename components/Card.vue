<template>
  <div class="w-full mx-auto max-w-3xl bg-white shadow p-8 text-gray-700">
    <h2 v-if="title" class="w-full text-3xl font-bold leading-tight mb-8">
      {{ title }}
    </h2>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "",
    },
  },
};
</script>

<style></style>
