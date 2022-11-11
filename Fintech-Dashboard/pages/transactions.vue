<template>
  <div class="app">
    <b-row class="top-name">
      <b-col class="top-text" md="4">
        <div class="all-stuffs">
          <div class="head">
            <p class="heading">PRIMARY</p>
          </div>
          <div class="text">
            <Buy />
          </div>
        </div>

        <div class="vertical"></div>
      </b-col>

      <b-col class="top-text sec" md="4">
        <div class="all-stuffs">
          <div class="head">
            <p class="heading">SECONDARY</p>
          </div>

          <div class="text">
            <Sell />
          </div>
        </div>

        <div class="vertical"></div>
      </b-col>

      <b-col class="top-text ter" md="4">
        <div class="all-stuffs">
          <div class="head">
            <p class="heading">TERTIARY</p>
          </div>

          <div class="text">
            <Invest />
          </div>
        </div>
      </b-col>
    </b-row>

    <b-row class="table">
      <b-col mb="12" class="overview">
        <div class="head-2">
          <p class="title">OVERVIEW</p>

          <p class="date">updated at <strong>8:01am on May 23</strong></p>
        </div>
      </b-col>
    </b-row>

    <b-row>
      <b-col md="12">
        <Table2 />
      </b-col>
    </b-row>
  </div>
</template>

<script>
import One from "../components/one.vue";
import Two from "../components/two.vue";
import Three from "../components/three.vue";
import Four from "../components/four.vue";
import Buy from "../components/buy.vue";
import Sell from "../components/sell.vue";
import Invest from "../components/invest.vue";
export default {
  name: "IndexPage",
  components: { One, Two, Three, Four, Buy, Sell, Invest },
};
</script>

<style scoped>
.top-name {
  margin-top: 30px;
}

.top-text {
  display: flex;
  justify-content: space-between;
  padding: 0px;
}

.all-stuffs {
  display: flex;
  flex-direction: column;
  flex: 0 0 99.5%;
}

.head {
  background: #f3f4f9;
}

.head p {
  padding: 40px 0px 20px 30px;
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  color: #a4a5b2;
}

.text {
  padding: 30px;
}

.vertical {
  border-left: 2px solid #e2e3e9;
  height: 100%;
}

.overview {
  padding: 30px;
  background: #f3f4f9;
}

.head-2 {
  display: flex;
  justify-content: space-between;
}
p.title {
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  color: #a4a5b2;
}

p.date {
  font-style: italic;
  font-weight: 500;
  font-size: 12px;
  color: #a4a5b2;
}

.fill-forms {
  display: flex;
}

@media only screen and (max-width: 600px) {
  .vertical {
    display: none;
  }

  .sec,
  .ter {
    display: none;
  }
}
</style>
