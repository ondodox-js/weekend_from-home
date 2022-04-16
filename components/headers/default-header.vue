<template>
  <header class="w-full h-[67px] absolute bg-white z-10">
    <div
      class="px-[17px] md:px-[213px] w-full max-w-8xl relative py-[17px] m-auto flex items-center"
    >
      <img
        src="~/assets/images/avatars/profile.png"
        class="w-[33px] h-[33px]"
        alt=""
      />
      <div class="flex flex-col justify-between absolute ml-12">
        <span class="text-xs">{{ date }}</span>
        <span class="font-bold">Fellas</span>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      date: "",
    };
  },
  mounted() {
    var today = new Date();
    var hours = today.getHours();

    if (hours < 12) {
      this.date = "Good Morning";
    } else if (hours < 18) {
      this.date = "Good Afternoon";
    } else {
      this.date = "Good Evening";
    }
  },
};
</script>

<style></style>
