<template>
  <div class="px-8 sm:px-0 sm:mx-[213px] text-left py-8 relative z-10">
    <h3 class="text-3xl font-bold sm:text-center mb-7">Help & Tips</h3>
    <div class="grid grid-cols-1 sm:grid-cols-3 gap-[10px]">
      <help-tips
        text="Start quickly with simple steps"
        :background="background"
      />
      <help-tips
        :background="background2"
        text="Run smoothly at vero eos et accusamus"
      />
      <help-tips
        :background="background3"
        text="Denounce with righteous indignation"
      />
    </div>
  </div>
</template>

<script>
import background from "../../assets/images/cards/weekend-ied-final.png";
import background3 from "../../assets/images/cards/weekend-ied-final2.png";
import background2 from "../../assets/images/cards/weekend-ied-final3.png";
import helpTips from "../cards/help-tips.vue";
export default {
  components: { helpTips },
  data() {
    return {
      background,
      background2,
      background3,
    };
  },
};
</script>
