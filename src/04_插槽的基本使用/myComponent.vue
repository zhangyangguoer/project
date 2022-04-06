<template>
  <div>
    <h2>组件开始</h2>
    <!-- 若定义多个slot插槽，当传入多个元素时，会每个插槽都会拥有传入的元素，不会一一对应 -->
    <slot>
      <i>展示默认自定义数据</i>
    </slot>
    <h2>组件结束</h2>
  </div>
</template>

<script>
export default {
};
</script>

<style scoped>
</style>