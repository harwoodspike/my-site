<template>
  <div :class="['flex-wrap', { 'mb-6 flex': !inline, 'inline-flex': inline }]">
    <div
      :class="[
        'relative w-full appearance-none',
        { 'label-floating': !inline },
      ]"
    >
      <component
        :is="fieldTag"
        :id="id"
        :class="[
          'tracking-wide leading-relaxed appearance-none w-full px-4 bg-gray-200 border border-gray-200 rounded focus:outline-none focus:bg-white focus:border-gray-500',
          { 'mb-3 py-2 block': !inline },
        ]"
        :type="fieldType"
        :placeholder="placeholder"
        :required="required"
      ></component>
      <label
        v-if="!inline"
        :for="id"
        class="absolute tracking-wide opacity-0 block top-0 left-0 cursor-text mb-4 leading-tight py-2 px-4"
        >{{ label }}
      </label>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    fieldTag: {
      type: String,
      required: true,
    },
    fieldType: {
      type: String,
      default: "",
    },
    id: {
      type: String,
      required: true,
    },
    placeholder: {
      type: String,
      default: "",
    },
    label: {
      type: String,
      required: true,
    },
    required: {
      type: Boolean,
      default: false,
    },
    inline: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
/* RED BORDER ON INVALID INPUT */
.check input:invalid {
  border-color: red;
}

/* FLOATING LABEL */
.label-floating input:not(:placeholder-shown),
.label-floating textarea:not(:placeholder-shown) {
  padding-top: 1.4rem;
}
.label-floating input:not(:placeholder-shown) ~ label,
.label-floating textarea:not(:placeholder-shown) ~ label {
  font-size: 0.8rem;
  transition: all 0.2s ease-in-out;
  color: #1f9d55;
  opacity: 1;
}
</style>
