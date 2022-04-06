<template>
  <div></div>
</template>

<script>
import emitter from "./utils/eventbus";
export default {
  name: "HomeContent",
  created() {
    emitter.on("eventName", (info) => {
      console.log("eventName:", info);
    });
    emitter.on("test", (info) => {
      console.log("test:", info);
    });
    emitter.on("*", (type, info) => {
      console.log("*:", type, info);
    });

    // 取消全部监听
    emitter.all.clear();
    // 取消某个监听（必传一个回调函数）
    function bymyself() {}
    emitter.on("eventName", bymyself); //监听
    emitter.off("eventName", bymyself); //取消监听
  },
};
</script>

<style lang="scss" scoped>
</style>