<!-- https://cn.vuejs.org/tutorial/#step-3 -->

<script>
export default {
  data() {
    return {
      titleClass: "title",
    };
  },
};
</script>

<template>
  <h1 :class="titleClass">Make me red</h1>
</template>

<style>
.title {
  color: red;
}
</style>
