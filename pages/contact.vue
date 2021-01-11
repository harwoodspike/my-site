<template>
  <Card title="Contact">
    <form :class="{ check: invalid }" @invalid.capture="invalid = true">
      <Field
        id="name"
        label="Name"
        field-tag="input"
        field-type="text"
        placeholder="Your Name"
        :required="true"
      />

      <Field
        id="email"
        label="Email"
        field-tag="input"
        field-type="email"
        placeholder="Your Email"
        :required="true"
      />

      <Field
        id="message"
        label="Message"
        field-tag="textarea"
        field-type="text"
        placeholder="Message..."
      />

      <button
        class="w-full shadow bg-teal-400 hover:bg-teal-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded"
        type="submit"
      >
        Send
      </button>
    </form>
  </Card>
</template>

<script>
export default {
  data: () => ({
    invalid: false,
  }),
};
</script>

<style></style>
