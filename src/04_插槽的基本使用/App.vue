<template>
  <div>
    <my-component>
      <span>测试测试</span>
    </my-component>
    <my-component> 纯文本展示 </my-component>
    <my-component>
      <my-button></my-button>
    </my-component>
    <!-- 不加值则会展示默认数据 -->
    <my-component> </my-component>
    <!-- 一个插槽可以添加多个 -->
    <my-component>
      <h3>1111</h3>
      <h3>2222</h3>
      <h3>3333</h3>
    </my-component>
  </div>
</template>

<script>
import myButton from "./myButton.vue";
import myComponent from "./myComponent.vue";
export default {
  components: { myButton, myComponent },
};
</script>

<style scoped>
</style>