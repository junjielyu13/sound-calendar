<!-- https://cn.vuejs.org/tutorial/#step-14 -->

<script>
import ChildComp from "./ChildComp.vue";

export default {
  components: {
    ChildComp,
  },
  data() {
    return {
      msg: "from parent",
    };
  },
};
</script>

<template>
  <ChildComp>Message: {{ msg }}</ChildComp>
</template>
