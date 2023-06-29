<template>
  <button type="button" @click="clickButton">{{ text }}</button>
</template>

<script>
export default {
  props: {
    text: { type: String, default: null },
    color: { type: Number, default: null },
    backGround: { type: String, default: "white" },
    borderRadius: { type: Number, default: "10px" },
  },
  emits: ["click"],
  setup(_, { emit }) {
    const clickButton = () => {
      console.log("emit");
      emit("click");
    };
    return { clickButton };
  },
};
</script>


<style lang="scss" scoped>
button {
  background-color: v-bind(backGround);
  border-color: v-bind(backGround);
  color: v-bind(color);
  border-radius: v-bind(borderRadius);
}
</style>