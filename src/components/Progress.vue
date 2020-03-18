<template>
  <div id="progress-bar">
    <ProgressPie :options="chartdata" :chart-data="chartdata"></ProgressPie>
    <ProgressPie></ProgressPie>
    <ProgressPie></ProgressPie>
  </div>
</template>

<script>
import ProgressPie from "@/components/ProgressPie.vue";

export default {
  name: "Progress",
  components: {
    ProgressPie
  },
  data() {
    return {
      chartdata: {
        datasets: [
          {
            data: [30, 70],
            backgroundColor: ["#919191", "#53e780"]
          }
        ],
        // These labels appear in the legend and in the tooltips when hovering different arcs
        labels: ["Red", "Yellow"]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        rotation: -0.5 * Math.PI - (-35 / 180) * Math.PI
      }
    };
  },
  mounted() {}
};
</script>

<style scoped>
#progress-bar {
  display: flex;
  width: 100vw;
  max-width: 100vw;
}
#progress-bar * {
  width: 33%;
}
</style>
