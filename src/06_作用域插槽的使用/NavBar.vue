<template>
  <div>
    <div v-for="(item, index) in selfName" :key="index">
      <slot :item="item" :index="index"></slot>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    selfName: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style scoped>
.nav-bar {
  display: flex;
}
.left,
.right {
  width: 80px;
  background-color: aquamarine;
}
.center {
  flex: 1;
  background-color: #212455;
}
</style>