<template>
  <div
    class="h-44 bg-cover relative"
    :style="`background-image: url(${background})`"
  >
    <div
      class="h-[72px] w-full absolute bottom-0 bg-black bg-opacity-50 py-[17px] px-5 flex items-center leading-none"
    >
      <span class="flex-1">{{ text }}</span>
      <button
        class="rounded-full relative w-8 h-8 flex justify-center bg-white items-center"
      >
        <div
          class="absolute w-full h-full bg-black rounded-full bg-opacity-60 hover:bg-opacity-0 z-10"
        ></div>
        <img
          src="~/assets/images/icons/right-arrow.svg"
          class="w-[11.2px] m-auto"
          alt=""
        />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["background", "text"],
};
</script>

<style></style>
