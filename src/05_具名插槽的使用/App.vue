<template>
  <div>
    <nav-bar :selfName="name">
      <!-- 具名插槽 语法糖：v-slot: === # -->
      <template v-slot:left>
        <span>left</span>
      </template>
      <template #center>
        <span>center</span>
      </template>
      <template v-slot:right>
        <span>right</span>
      </template>
      <!-- 复杂业务：使用父子组件传值，将自定义插槽名称传给子组件，实现动态定义具名插槽 -->
      <template #[name]> 动态定义具名插槽 </template>
    </nav-bar>
  </div>
</template>

<script>
import NavBar from "./NavBar.vue";
export default {
  components: { NavBar },
  data() {
    return {
      name: "byself",
    };
  },
};
</script>

<style scoped>
</style>