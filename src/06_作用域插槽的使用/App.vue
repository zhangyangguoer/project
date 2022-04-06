<template>
  <div>
    <nav-bar :selfName="names">
      <template v-slot="slotProps">
        <button>{{ slotProps.item }}</button>
      </template>
    </nav-bar>
  </div>
</template>

<script>
import NavBar from "./NavBar.vue";
export default {
  components: { NavBar },
  data() {
    return {
      names: ["byself", "code", "why", "james"],
    };
  },
};
</script>

<style scoped>
</style>