<template>
  <div class="nav-bar">
    <div class="left">
      <slot name="left"></slot>
    </div>
    <div class="center">
      <slot name="center"></slot>
    </div>
    <div class="right">
      <slot name="right"></slot>
    </div>
    <div>
      <slot :name="selfName"></slot>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    selfName: String,
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