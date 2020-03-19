<template>
  <div id="progress-bar">
    <div class="point-box">
      <ProgressPie :options="options[0]" :chart-data="chartdata[0]"></ProgressPie>
      <h1>
        {{
        Math.ceil(
        (chartdata[0].datasets[0].data[1] /
        (chartdata[0].datasets[0].data[0] +
        chartdata[0].datasets[0].data[1])) *
        100
        )
        }}
        %
      </h1>
    </div>
    <div class="point-box">
      <ProgressPie :options="options[1]" :chart-data="chartdata[1]"></ProgressPie>
      <h1>
        {{
        Math.ceil(
        (chartdata[1].datasets[0].data[1] /
        (chartdata[1].datasets[0].data[0] +
        chartdata[1].datasets[0].data[1])) *
        100
        )
        }}
        %
      </h1>
    </div>
    <div class="point-box">
      <ProgressPie :options="options[2]" :chart-data="chartdata[2]"></ProgressPie>
      <h1>
        {{
        Math.ceil(
        (chartdata[2].datasets[0].data[1] /
        (chartdata[2].datasets[0].data[0] +
        chartdata[2].datasets[0].data[1])) *
        100
        )
        }}
        %
      </h1>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import ProgressPie from "@/components/ProgressPie.vue";

export default {
  name: "Progress",
  components: {
    ProgressPie
  },
  data() {
    return {
      chartdata: [
        {
          datasets: [
            {
              data: [0, 100],
              backgroundColor: ["#919191", "#53e780"],
              hoverBackgroundColor: ["#FF5A5E", "#FFC870"]
            }
          ],
          labels: []
        },
        {
          datasets: [
            {
              data: [50, 50],
              backgroundColor: ["#919191", "#53e780"],
              hoverBackgroundColor: ["#FF5A5E", "#FFC870"]
            }
          ],
          labels: []
        },
        {
          datasets: [
            {
              data: [60, 40],
              backgroundColor: ["#919191", "#53e780"],
              hoverBackgroundColor: ["#FF5A5E", "#FFC870"]
            }
          ],
          labels: []
        }
      ],
      options: [
        {
          title: {
            display: true,
            text: "Этап 1. ПЕРСОНА",
            position: "bottom",
            fontSize: 16,
            fontColor: "black",
            fontFamily: "'Roboto Light', sans-serif"
          },
          layout: {
            padding: {
              left: 0,
              right: 0,
              top: 16,
              bottom: 0
            }
          },
          responsive: true,
          maintainAspectRatio: false,
          rotation: -0.5 * Math.PI - (270 / 180) * Math.PI,
          legend: {
            display: false,
            hidden: true,
            labels: {
              display: false,
              fontColor: "rgb(255, 99, 132)"
            }
          },
          tooltips: {
            enabled: false
          }
        },
        {
          title: {
            display: true,
            text: "Этап 2. ПРОДУКТ",
            position: "bottom",
            fontSize: 16,
            fontColor: "black",
            fontFamily: "'Roboto Light', sans-serif"
          },
          layout: {
            padding: {
              left: 0,
              right: 0,
              top: 16,
              bottom: 0
            }
          },
          responsive: true,
          maintainAspectRatio: false,
          rotation: -0.5 * Math.PI - (270 / 180) * Math.PI,
          legend: {
            display: false,
            hidden: true,
            labels: {
              display: false,
              fontColor: "rgb(255, 99, 132)"
            }
          },
          tooltips: {
            enabled: false
          }
        },
        {
          title: {
            display: true,
            text: "Этап 3. ЦЕЛЕВАЯ АУДИТОРИЯ",
            position: "bottom",
            fontSize: 16,
            fontColor: "black",
            fontFamily: "'Roboto Light', sans-serif"
          },
          layout: {
            padding: {
              left: 0,
              right: 0,
              top: 16,
              bottom: 0
            }
          },
          responsive: true,
          maintainAspectRatio: false,
          rotation: -0.5 * Math.PI - (270 / 180) * Math.PI,
          legend: {
            display: false,
            hidden: true,
            labels: {
              display: false,
              fontColor: "rgb(255, 99, 132)"
            }
          },
          tooltips: {
            enabled: false
          }
        }
      ]
    };
  }
};
</script>

<style scoped>
#progress-bar {
  display: flex;
  width: 100vw;
  max-width: 100vw;
  max-height: 20vh;
  box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.2);
  justify-content: space-between;
}
#progress-bar .point-box {
  max-width: 33%;
  max-height: 20vh;
}
.point-box {
  display: flex;
  position: relative;
  margin: auto;
  width: 33vw;
}
.point-box h1 {
  position: absolute;
  top: 30%;
  width: 100%;
  text-align: center;
  color: #fff;
  font-size: 3.6vh;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.6);
}
.point-box h1::after {
  content: "";
  display: block;
  position: absolute;
  top: calc(0px + 1rem);
  width: 66%;
  height: 1px;
  background-image: url("data:image/svg+xml,%3csvg width='100%25' height='100%25' xmlns='http://www.w3.org/2000/svg'%3e%3crect width='100%25' height='100%25' fill='none' stroke='%23757575FF' stroke-width='4' stroke-dasharray='6%2c 14' stroke-dashoffset='0' stroke-linecap='square'/%3e%3c/svg%3e");
  z-index: -1;
}

.point-box div {
  display: flex;
}
.point-box div {
  margin: 0 auto;
}
.point-box h1::before {
  left: 0;
}
.point-box:first-child h1::before,
.point-box:last-child h1::after {
  display: none;
}
.point-box h1::after {
  right: -32%;
}

.point-box canvas {
  margin: auto auto;
}
.dashed-row {
  border: 10px dashed black;
  width: 100px;
  height: 1px;
  margin: auto;
  background-color: #4d4d4d;
}
</style>
