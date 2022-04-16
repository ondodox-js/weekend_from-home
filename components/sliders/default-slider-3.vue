<template>
  <div
    class="max-w-3xl w-full m-auto sm:px-16 pl-8 pr-0 relative top-[-6.5rem]"
  >
    <h3 class="text-3xl font-bold sm:text-center mb-7">Testimonial</h3>
    <div class="glide text-black">
      <div class="glide__track overflow-hidden" data-glide-el="track">
        <ul class="glide__slides grid grid-flow-col grid-cols-1">
          <li class="glide__slide" v-for="tester of testers" :key="tester.id">
            <testimonial :tester="tester" />
          </li>
        </ul>
      </div>
      <div
        class="glide__arrows text-white hidden absolute sm:flex sm:justify-between bottom-14 left-0 w-full"
        data-glide-el="controls"
      >
        <button
          class="glide__arrow glide__arrow--left rounded-full relative w-8 h-8 flex justify-center bg-white items-center"
          data-glide-dir="<"
        >
          <div
            class="absolute w-full h-full bg-black bg-opacity-60 hover:bg-opacity-0 z-10"
          ></div>
          <img
            src="~/assets/images/icons/right-arrow.svg"
            class="w-[11.2px] m-auto rotate-180"
            alt=""
          />
        </button>
        <button
          class="glide__arrow glide__arrow--right rounded-full relative w-8 h-8 flex justify-center bg-white items-center"
          data-glide-dir=">"
        >
          <div
            class="absolute w-full h-full bg-black bg-opacity-60 hover:bg-opacity-0 z-10"
          ></div>
          <img
            src="~/assets/images/icons/right-arrow.svg"
            class="w-[11.2px] m-auto"
            alt=""
          />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import Glide from "@glidejs/glide";
import testimonial from "../cards/testimonial.vue";
export default {
  components: { testimonial },
  data() {
    return {
      testers: null,
    };
  },
  async mounted() {
    await fetch(
      "https://wknd-take-home-challenge-api.herokuapp.com/testimonial"
    )
      .then((resp) => resp.json())
      .then((result) => (this.testers = result))
      .catch((e) => console.log(e));

    const config = {
      type: "slider",
      startAt: 0,
      perView: 2.5,
      direaction: "ltr",
      breakpoints: {
        640: {
          perView: 1.5,
        },
      },
    };
    new Glide(".glide", config).mount();
  },
};
</script>
