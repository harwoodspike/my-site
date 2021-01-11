<template>
  <div
    class="border border-blue-100 shadow rounded-md p-4 max-w-sm w-full mx-auto"
  >
    <div class="animate-pulse flex space-x-4">
      <div v-if="templateType == 'text'" class="flex-1 space-y-4 py-1">
        <div class="h-4 bg-blue-300 rounded w-3/4"></div>
        <div class="space-y-2">
          <div class="h-4 bg-blue-300 rounded"></div>
          <div class="h-4 bg-blue-300 rounded w-5/6"></div>
        </div>
      </div>
      <div v-else-if="templateType == 'image'" class="flex-1 space-y-4 py-1">
        <div class="h-24 bg-blue-300 rounded"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    templateType: {
      type: String,
      default: "text",
    },
  },
};
</script>

<style></style>
