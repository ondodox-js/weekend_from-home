<template>
  <div class="max-w-2xl w-full m-auto text-left sm:text-center p-8">
    <h3 class="text-3xl font-bold">{{ title }}</h3>
    <p class="text-base sm:text-lg mt-7">
      {{ content }}
    </p>
  </div>
</template>

<script>
export default {
  props: ["title", "content"],
};
</script>

<style></style>
