<script>
import { Pie, mixins } from "vue-chartjs";
const { reactiveProp } = mixins;

export default {
  extends: Pie,
  mixins: [reactiveProp],
  props: ["options", "chartData"],
  data: () => ({}),
  mounted() {
    this.renderChart(this.chartData, this.options);
  }
};
</script>

<style scoped>
canvas {
  max-width: 33vw !important;
}
.color {
  background-color: #53e780;
}
</style>
