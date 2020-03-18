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
.color {
  background-color: #53e780;
}
</style>
