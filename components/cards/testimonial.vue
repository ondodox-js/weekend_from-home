<template>
  <div class="w-full h-full p-5 bg-white leading-none">
    <h3 class="text-3xl font-bold mb-5">{{ tester.by }}</h3>
    <span class="text-xs font-medium">{{ tester.testimony }}</span>
  </div>
</template>

<script>
export default {
  props: ["tester"],
};
</script>
