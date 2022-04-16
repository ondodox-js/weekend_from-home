<template>
  <main class="w-full">
    <section class="bg-[#eebece] w-full">
      <div
        class="container-1 bg-cover sm:bg-auto sm:h-[768px] h-full max-w-8xl m-auto bg-no-repeat text-center text-white"
      >
        <div
          data-aos="fade-down"
          data-aos-duration="2000"
          class="pt-[123px] sm:pt-[8.1rem]"
        >
          <h1 class="uppercase text-[52px] sm:text-[62px] font-bold">
            weekend from home
          </h1>
          <span class="italic font-semibold text-xs sm:text-[21px]"
            >Stay active with a little workout.</span
          >
          <lego-button />
        </div>
      </div>
      <div class="w-full py-[152px] max-w-8xl m-auto relative">
        <img
          class="w-[76px] absolute top-0 right-0"
          src="~/assets/images/attributes/ginjal1_2.png"
          alt=""
        />
        <img
          class="w-24 absolute top-0 right-8 -rotate-90"
          src="~/assets/images/legos/1.png"
          alt=""
        />
        <div
          data-aos="fade-up"
          class="text-right text-base p-8 sm:text-xl max-w-2xl font-medium m-auto"
        >
          <p>
            <span class="text-[#0B24FB] font-bold">Deffinition;</span> a
            practice or exercise to test or improve one's fitness for athletic
            competition, ability, or performance to exhaust (something, such as
            a mine) by working to devise, arrange, or achieve by resolving
            difficulties. Merriam-Webster.com Dictionary.
          </p>
          <p class="italic text-white mt-5 sm:mt-[30px]">-weekend team</p>
        </div>
      </div>
    </section>
    <section class="bg-black w-full text-white">
      <div class="max-w-8xl m-auto relative">
        <img
          src="~/assets/images/attributes/lingkaran-blue.png"
          class="w-[89px] absolute -top-44 left-[15%] sm:left-[18%]"
        />
        <default-slider-3 data-aos="fade-up" />
        <label-paragraf
          data-aos="fade-right"
          data-aos-duration="1500"
          class="pt-0"
          title="POV"
          content="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud ullamco laboris nisi ea commodo
            consequat. Duis aute irure dolor in reprehenderit in voluptate velit
            esse cillum dolore eu fugiat nulla pariatur."
        />
        <label-paragraf
          data-aos="fade-left"
          data-aos-duration="1500"
          title="Resource"
          content="These cases are perfectly simple and easy to distinguish. In a free hour, when our power of choice is untrammelled and when nothing prevents our being able to do what we like best"
        />
        <label-card-3 />
        <label-paragraf
          title="You're all set."
          content="The wise man therefore always holds in these matters to this principle of selection."
        />
        <div class="relative sm:pt-0 pt-8 bottom-0 left-0 sm:h-40">
          <img
            src="~/assets/images/attributes/image-lb.png"
            class="w-[244px] sm:absolute bottom-0 left-0"
            alt=""
          />
        </div>
        <img
          src="~/assets/images/attributes/ginjal1.png"
          class="hidden sm:block absolute bottom-[32%] right-[10%] -scale-x-100 w-[159px]"
        />
      </div>
    </section>
  </main>
</template>

<script>
import legoButton from "../components/legos/lego-button.vue";
import DefaultSlider3 from "../components/sliders/default-slider-3.vue";
import LabelCard3 from "../components/text-content/label-card-3.vue";
import LabelParagraf from "../components/text-content/label-paragraf.vue";
import AOS from "aos";
export default {
  mounted() {
    AOS.init({});
  },
  components: { legoButton, LabelParagraf, LabelCard3, DefaultSlider3 },
};
</script>
<style scoped>
.container-1 {
  background-image: url("/images/background/mobile-1.png");
}
@media screen and (min-width: 640px) {
  .container-1 {
    background-image: url("/images/background/desktop-1.png");
  }
}
</style>
