<template>
  <div>
    <div class="head">
      <div class="name">
        <h6>TECHNOLOGY</h6>
      </div>

      <div class="date">
        <p>updated at <strong> on Jan 23 </strong></p>
      </div>
    </div>

    <div class="roi">
      <h2>27.24 <mark> ROI </mark></h2>
    </div>

    <div class="graph-2">
      <canvas id="myChart2"></canvas>
    </div>

    <div class="list">
      <div class="item">
        <div class="wrap">
          <div class="high all"></div>
          <p class="title">Cloud Services</p>
        </div>
        <div class="percent"><p>61%</p></div>
      </div>
      <hr />
      <div class="item">
        <div class="wrap">
          <div class="mid all"></div>
          <p class="title">Automation</p>
        </div>
        <div class="percent"><p>28%</p></div>
      </div>
      <hr />
      <div class="item">
        <div class="wrap">
          <div class="low all"></div>
          <p class="title">Business Transformation</p>
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
    const ctx = document.getElementById("myChart2").getContext("2d");
    const myChart = new Chart(ctx, {
      type: "bar",
      data: {
        labels: [
          "a",
          "b",
          "c",
          "d",
          "e",
          "f",
          "g",
          "h",
          "i",
          "j",
          "k",
          "l",
          "m",
          "n",
          "o",
          "p",
        ],
        datasets: [
          {
            label: "Technology",
            data: [12, 19, 3, 5, 2, 3, 9, 13, 12, 19, 3, 5, 2, 3, 9, 13],
            backgroundColor: ["#000AFF", "rgba(0, 71, 255, 0.5)"],
          },
        ],
      },
      options: {
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
            grid: {
              display: false,
              drawTicks: false,
              drawOnChartArea: false,
            },
          },
          x: {
            grid: {
              display: false,
              drawTicks: false,
              drawOnChartArea: false,
            },
          },
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
  margin-top: 12px;
  height: 116px;
}

.list {
  margin-top: 62px;
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
  background: #000aff;
}

.mid {
  background: rgba(0, 71, 255, 0.5);
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

@media only screen and (max-width:600px){ 
  .list {
  margin-top: 30%;
}
}
</style>
