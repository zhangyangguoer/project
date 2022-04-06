<template>
  <div class="tab-control">
    <div
      v-for="(title, index) in titles"
      :key="index"
      class="tab-item"
      @click="tabClick(index)"
    >
      <span class="tab-span" :class="{ active: currentIndex == index }">{{
        title
      }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabControl",
  props: {
    titles: {
      type: Array,
      default: () => [],
    },
  },
  emits: ["clickCurrent"],
  data() {
    return {
      currentIndex: 0,
    };
  },
  methods: {
    tabClick(index) {
      this.currentIndex = index;
      this.$emit("clickCurrent", index);
    },
  },
};
</script>

<style scoped>
.tab-control {
  display: flex;
}
.tab-item {
  flex: 1;
  text-align: center;
}
.active {
  color: red;
  border-bottom: 3px solid red;
  padding: 5px 10px;
}
</style>
