<script>
import { Bar } from "vue-chartjs";
import "chartjs-plugin-colorschemes";
import { RdPu4 } from "chartjs-plugin-colorschemes/src/colorschemes/colorschemes.brewer";

export default {
  extends: Bar,
  props: {
    chartdata: {
      type: Object,
      default: null,
    },
  },
  data: () => ({
    options: {
      legend: {
        position: "bottom",
        align: "start",
      },
      plugins: {
        colorschemes: {
          scheme: RdPu4,
        },
      },
    },
  }),
  mounted() {
    this.renderChart(this.chartdata, this.options);
  },
};
</script>