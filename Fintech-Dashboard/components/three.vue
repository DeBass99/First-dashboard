<template>
  <div>
    <div class="head">
      <div class="name">
        <h6>HEALTHCARE</h6>
      </div>

      <div class="date">
        <p>updated at <strong> on Jan 23 </strong></p>
      </div>
    </div>

    <div class="roi">
      <h2>16.35 <mark> ROI </mark></h2>
    </div>

    <div class="graph-2">
      <canvas id="myChart3"></canvas>
    </div>

    <div class="list">
      <div class="item">
        <div class="wrap">
          <div class="high all"></div>
          <p class="title">Pharmaceutical</p>
        </div>
        <div class="percent"><p>61%</p></div>
      </div>
      <hr />
      <div class="item">
        <div class="wrap">
          <div class="mid all"></div>
          <p class="title">Services and Facilities</p>
        </div>
        <div class="percent"><p>28%</p></div>
      </div>
      <hr />
      <div class="item">
        <div class="wrap">
          <div class="low all"></div>
          <p class="title">Equipment</p>
        </div>
        <div class="percent"><p>11%</p></div>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js/auto";
export default {
  mounted() {
    const ctx = document.getElementById("myChart3").getContext("2d");
    const myChart = new Chart(ctx, {
      type: "line",
      data: {
        labels: ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11"],
        datasets: [
          {
            label: "Healthcare",
            data: [6, 5, 9, 6, 8, 7, 9, 10, 7, 9, 3],
            backgroundColor: ["rgba(255, 0, 0, 0.51)"],
          },
          {
            label: "Technology",
            data: [6, 9, 6, 5, 8, 6, 10, 7, 5, 9, 6],
            backgroundColor: ["rgba(255, 0, 0, 0.51)"],
          },
        ],
      },
      options: {
        elements: {
          line: {
            fill: true,
          },
        },
        plugins: {
          legend: {
            display: false,
          },
        },
        scales: {
          y: {
            ticks: {
              display: false,
            },
          },

          x: {},
        },
      },
    });
  },
};
</script>

<style scoped>
.head {
  display: flex;
  justify-content: space-between;
}

.head h3 {
  font-style: normal;
  font-weight: 700;
  font-size: 13px;
  color: #3f404a;
}

.head p {
  font-style: italic;
  font-weight: 400;
  font-size: 12px;
  color: #a4a5b2;
}

.roi h2 {
  font-style: normal;
  font-weight: 600;
  font-size: 19px;
  color: #3f404a;
}

mark {
  background: none;
  font-size: 14px;
  color: #a5a9c1;
}

.graph-2 {
  text-align: center;
  margin-top: 22px;
  height: 116px;
}

.list {
  margin-top: 52px;
}

.wrap {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.item {
  display: flex;
  justify-content: space-between;
}

.all {
  width: 8px;
  height: 8px;
  border-radius: 4px;
}

.high {
  background: rgba(239, 0, 0, 0.94);
}

.mid {
  background: rgba(255, 0, 0, 0.51);
}

.low {
  background: #a4a5b2;
  opacity: 0.2;
}
p.title {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #3f404a;
  margin-left: 14px;
  margin-bottom: 0px;
}

.percent p {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #a4a5b2;
}

img {
  width: 100%;
}

@media only screen and (max-width: 600px) {
  .list {
    margin-top: 30%;
  }
}
</style>
