<template>
  <div>
    <tab-control :titles="titles" @clickCurrent="clickCurrent"></tab-control>
    <h2>{{ contents[currentIndex] }}</h2>
  </div>
</template>

<script>
import TabControl from "./components/tabControl.vue";

export default {
  name: "App",
  components: {
    TabControl,
  },
  data() {
    return {
      titles: ["衣服", "包包", "鞋子"],
      contents: ["衣服页面", "包包页面", "鞋子页面"],
      currentIndex:0,
    };
  },
  methods:{
    clickCurrent(index){
      this.currentIndex = index;
    }
  }
};
</script>

<style>
</style>
