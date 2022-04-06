<template>
  <div>
    <button @click="clickButton">mitt使用</button>
  </div>
</template>

<script>
import emitter from "./utils/eventbus";
export default {
  name: "About",
  methods: {
    clickButton() {
      emitter.emit("eventName", { name: "test", age: 19 });
      emitter.emit("test", { name: "practice", age: 98 });
    },
  },
};
</script>

<style lang="scss" scoped>
</style>