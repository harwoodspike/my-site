<template>
  <div class="h-screen flex flex-col justify-center items-center">
    <Skeleton template-type="image"></Skeleton>
    <!-- <Image
        src="https://placeimg.com/500/300/nature"
        alt="A random nature image"
        ratio="16by9"
        :lazy="false"
      >
        <Skeleton
          slot="placeholder"
          class="skeleton-placeholder"
          height="100%"
        ></Skeleton>
      </Image> -->
    <h1 class="title">Joshua Harwood</h1>
    <div class="links">
      <ALink href="https://facebook.com/">Facebook</ALink>
      <ALink href="https://twitter.com/">Twitter</ALink>
      <ALink href="https://linkedin.com/">LinkedIn</ALink>
      <ALink href="https://github.com/">Github</ALink>
      <ALink href="https://bitbucket.com/">Bitbucket</ALink>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  layout: "home",
});
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
