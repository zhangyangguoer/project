<template>
  <div>
    <Home></Home>
    <button @click="addName">AddName</button>
  </div>
</template>

<script>
import Home from "./Home.vue";
import { computed } from "vue";
export default {
  name: "App",
  components: {
    Home,
  },
  provide() {
    return {
      name: "Jim",
      age: "10",
      length: computed(() => this.name.length), // 返回ref对象  取值是：.value
    };
  },
  data() {
    return {
      name: ["corder why", "skj", "asjk"],
    };
  },
  methods: {
    addName() {
      this.name.push("why");
    },
  },
};
</script>

<style lang="scss" scoped>
</style>