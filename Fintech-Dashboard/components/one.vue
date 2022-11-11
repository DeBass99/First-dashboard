<template>
  <div>
    <div class="graph-1">
      <p>Overview Status</p>
      <div class="chart">
        <canvas id="myChart"></canvas>
      </div>
    </div>

    <div class="list">
      <div class="item">
        <div class="wrap">
          <div class="tech all"><p>TECH</p></div>
          <p class="title">Technology</p>
        </div>
        <div class="percent"><p>26%</p></div>
      </div>
      <hr />
      <div class="item">
        <div class="wrap">
          <div class="health all"><p>HLTH</p></div>
          <p class="title">Healthcare</p>
        </div>
        <div class="percent"><p>9%</p></div>
      </div>
      <hr />
      <div class="item">
        <div class="wrap">
          <div class="energy all"><p>ENRG</p></div>
          <p class="title">Energy</p>
        </div>
        <div class="percent"><p>65%</p></div>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js/auto";

export default {
  mounted() {
    const ctx = document.getElementById("myChart").getContext("2d");
    const myChart = new Chart(ctx, {
      type: "doughnut",
      circumference: 3,
      data: {
        datasets: [
          {
            label: "Overview",
            data: [150, 300, 30],
            backgroundColor: [
              "rgb(0, 10, 255)",
              "rgba(164, 165, 178, 0.3)",
              "rgba(239, 0, 0, 0.94)",
            ],
            hoverOffset: 4,
          },
        ],
      },
      options: {
        cutout: 50,
      },
    });
  },
};
</script>

<style scoped>
.graph-1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.graph-1 p {
  font-style: normal;
  font-weight: 700;
  font-size: 13px;
}

.graph-1 img {
  width: 160px;
  height: 160px;
}

.list {
  margin-top: 60px;
}

.wrap {
  display: flex;
  justify-content: flex-start;
}

.item {
  display: flex;
  justify-content: space-between;
}

.all {
  width: 48px;
  height: 24px;
  border-radius: 47px;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  display: flex;
  justify-content: center;
}
.tech {
  background: rgba(0, 71, 255, 0.1);
  color: #000aff;
}

.health {
  background: rgba(255, 0, 0, 0.25);
  color: #d91a1a;
}

.energy {
  background: #e2e3e9;
  color: #000;
}

p.title {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #3f404a;
  margin-left: 14px;
}

.percent p {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #a4a5b2;
}

.chart {
  width: 160px;
  height: 160px;
}
</style>
