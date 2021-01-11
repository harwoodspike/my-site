<template>
  <div class="box-border">
    <div class="flex float-right justify-items-center items-center h-6 mb-4">
      <Field
        v-if="search"
        id="search_value"
        label="Search"
        field-tag="input"
        field-type="text"
        placeholder="Search"
        :inline="true"
      ></Field>
      <font-awesome-icon
        class="text-lg m-1"
        :icon="['fas', 'search']"
        @click="search = !search"
      />
      <font-awesome-icon
        :class="[
          'text-lg text-gray-400 m-1',
          { 'text-gray-800': view === 'list' },
        ]"
        :icon="['fas', 'list']"
        @click="view = 'list'"
      />
      <font-awesome-icon
        :class="[
          'text-lg text-gray-200 m-1',
          { 'text-gray-800': view === 'grid' },
        ]"
        :icon="['fas', 'th-large']"
        @click="view = 'grid'"
      />
    </div>
    <div
      :class="[
        'grid w-full',
        {
          'grid-cols-2 lg:grid-cols-3': view === 'grid',
          'grid-cols-1': view !== 'grid',
        },
      ]"
    >
      <div
        v-for="item in items"
        :key="item.name"
        class="bg-gray-100 m-1 border-black border"
      >
        {{ item.name }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    view: "grid",
    search: false,
    items: [
      { name: "One" },
      { name: "Two" },
      { name: "Three" },
      { name: "Four" },
    ],
  }),
};
</script>

<style scoped></style>
