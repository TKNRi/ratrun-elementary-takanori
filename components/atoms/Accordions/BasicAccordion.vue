<template>
  <div class="accordion-box">
    <button @click="clickAccordion" class="accordion">アコーディオン</button>
    <div v-if="isAccordion" class="accordion-open">
      アコーディオン展開イメージ昨今、情報技術は目まぐるしい勢いで進化を続け、インターネットでは、1日に膨大な量の情報が飛び交っています。インターネットで現代人が1日に触れる情報量は江戸時代の1年分とも言われています。
    </div>
  </div>
</template>

<script>
//import { defineComponent } from "@vue/composition-api";

export default {
  setup() {
    const clickAccordion = () => {
      isAccordion.value = !isAccordion.value;
      //   if (isAccordion.value === true) {
      //     isAccorion.value = false;
      //   } else {
      //     isAccorion.value = true;
      //   }
    };
    const isAccordion = ref(false);
    return { isAccordion, clickAccordion };
  },
};
</script>

<style lang='scss' scoped>
.accordion-box {
  padding: 0 10%;
  display: block;
}
.accordion {
  margin-top: 20px;
  padding: 20px 0;
  background-color: #808080;
  width: 100%;
}
.accordion-open {
  background-color: #c0c0c0;
}
</style>
