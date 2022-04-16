<template>
  <div>
    <default-header />
    <Nuxt />
    <default-footer />
  </div>
</template>

<script>
import DefaultFooter from "../components/footers/default-footer.vue";
import defaultHeader from "../components/headers/default-header.vue";
export default {
  components: { defaultHeader, DefaultFooter },
};
</script>

<style></style>
