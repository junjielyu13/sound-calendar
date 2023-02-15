<!-- https://cn.vuejs.org/tutorial/#step-12 -->

<script>
import ChildComp from "./ChildComp.vue";

export default {
  components: {
    ChildComp,
  },
  data() {
    return {
      greeting: "Hello from parent",
    };
  },
};
</script>

<template>
  <ChildComp :msg="greeting" />
</template>
