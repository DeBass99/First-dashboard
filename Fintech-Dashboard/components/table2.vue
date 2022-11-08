<template>
  <div>
    <div class="table-all">
      <div>
        <div class="heading">
          <div class="two">
            <img src="~/assets/tick.png" alt="" class="tick" />
            <p>Investment Portfolio (%)</p>
          </div>
          <button class="btn"><img src="~/assets/button.png" alt="" /></button>
        </div>
        <hr />
        <table-list-2
          v-for="(detail, i) in details"
          :key="i"
          :market="detail.market"
          :percent="detail.percent"
          :color="detail.status"
          :color2="detail.stat"
        />
      </div>

      <div>
        <div class="heading">
          <div class="two">
            <img src="~/assets/tick.png" alt="" class="tick" />
            <p>Investment Portfolio ($)</p>
          </div>
          <button class="btn"><img src="~/assets/button.png" alt="" /></button>
        </div>
        <hr />
        <table-list-2
          v-for="(percent, i) in percents"
          :key="i"
          :market="percent.market"
          :percent="percent.percent"
          :color="percent.status"
          :color2="percent.stat"
        />
      </div>

      <div>
        <div class="heading">
          <div class="two">
            <img src="~/assets/tick.png" alt="" class="tick" />
            <p>Investment Portfolio (transactions)</p>
          </div>
          <button class="btn"><img src="~/assets/button.png" alt="" /></button>
        </div>
        <hr />
        <table-list-2
          v-for="(date, i) in dates"
          :key="i"
          :market="date.market"
          :percent="date.percent"
          :color="date.status"
        />
      </div>
    </div>
  </div>
</template>

<script>
import json from "~/js/investment.json";
import tableList2 from "./tableList2.vue";
export default {
  components: { tableList2 },
  data() {
    return {
      details: json["first"],
      percents: json["second"],
      dates: json["third"],
    };
  },
};
</script>

<style scoped>
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 10px;
  padding: 0px;
}

.two {
  display: flex;
  align-items: center;
}

img.tick {
  height: 11.179166793823242px;
  width: 14.654165267944336px;
  margin-top: -10px;
}

p {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #a4a5b2;
  margin-left: 8px;
}

button.btn {
  background: none;
  border: none;
  margin-left: 209px;
  margin-top: -10px;
  padding: 0px;
}

.table-all {
  display: flex;
  justify-content: space-between;
}
</style>
