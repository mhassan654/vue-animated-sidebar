<template>
  <div class="chart-renderer">
    <bar-chart :chartdata="series" />
  </div>
</template>

<script>
import BarChart from "./ChartComp.vue";
import moment from "moment";

export default {
  name: "ChartRenderer",
  components: { BarChart },
  props: {
    resultSet: {
      type: Object,
      required: true,
    },
  },
  data: () => ({
    loaded: false,
    chartdata: {},
  }),
  computed: {
    series() {
      //Transform data for visualization
      const labels = this.resultSet
        .seriesNames({
          x: [],
          y: ["Orders.createdAt"],
        })
        .map((column) => moment(column.yValues[0]).format("MMMM"));

      const datasets = this.resultSet.series().map((item) => {
        return {
          label: item.title,
          data: item.series.map((item) => item.value),
        };
      });
      return {
        labels,
        datasets,
      };
    },
  },
};
</script>