<script>
import AxisLabel from "./AxisLabel.vue";
import { valueToPoint } from "./util.js";

export default {
  components: {
    AxisLabel,
  },
  props: {
    stats: Array,
  },
  computed: {
    // 一个用于多边形顶点的计算属性
    points() {
      const total = this.stats.length;
      return this.stats
        .map((stat, i) => {
          const { x, y } = valueToPoint(stat.value, i, total);
          return `${x},${y}`;
        })
        .join(" ");
    },
  },
};
</script>

<template>
  <g>
    <polygon :points="points"></polygon>
    <circle cx="100" cy="100" r="80"></circle>
    <axis-label
      v-for="(stat, index) in stats"
      :stat="stat"
      :index="index"
      :total="stats.length"
    >
    </axis-label>
  </g>
</template>
