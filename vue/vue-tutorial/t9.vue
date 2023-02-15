<!-- https://cn.vuejs.org/tutorial/#step-9 -->

<script>
export default {
  mounted() {
    this.$refs.p.textContent = "mounted!";
  },
};
</script>

<template>
  <p ref="p">hello</p>
</template>
