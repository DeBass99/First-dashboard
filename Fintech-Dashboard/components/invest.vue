<template>
  <div class="app">
    <b-row class="all">
      <button class="choose">INVESTMENT IDEA</button>
      <form action="submit" class="form">
        <div class="sell-gp">
          <b-col class="buy">
            <div class="form-group">
              <label for="category">Category</label>
              <select class="form-control input-style" id="category">
                <option>EU Portfolio</option>
                <option>US Portfolio</option>
                <option>UK Portfolio</option>
                <option>NIG Portfolio</option>
                <option>CANADA Portfolio</option>
              </select>
            </div>

            <div class="form-group">
              <label for="marketplace">Marketplace</label>
              <select class="form-control input-style" id="category">
                <option>Bitcoin</option>
                <option>Nasdaq</option>
                <option>FTSE</option>
              </select>
            </div>

            <div class="form-group">
              <label for="budget">Budget</label>
              <input
                type="text"
                class="form-control"
                aria-label="Amount (to the nearest dollar)"
              />
              <i>$</i>
            </div>
          </b-col>

          <b-col class="sell">
            <div class="form-group">
              <label for="budget">Amount</label>
              <input
                type="text"
                class="form-control"
                aria-label="Amount (to the nearest dollar)"
              />
              <i>OCDO</i>
            </div>

            <div class="form-group">
              <label for="exampleFormControlSelect1">Timeline</label>
              <select class="form-control input-style" id="exampleFormControlSelect1">
                <option>1 Year</option>
                <option>2 Years</option>
                <option>3 Years</option>
                <option>4 Years</option>
                <option>5 Years</option>
              </select>
            </div>

            <div class="form-group">
              <button class="select">INVEST (PORTFOLIO)</button>
            </div>
          </b-col>
        </div>
      </form>
    </b-row>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.form-group {
  margin-top: 30px;
}

.buy-gp {
  display: flex;
  flex-direction: row;
}

.sell-gp {
  display: flex;
  flex-direction: row;
}

button.choose {
  width: 432px;
  padding: 12px 100px;
  background-color: #fff;
  border: 1px solid #e4e6ef;
  font-style: normal;
  font-weight: 400;
  font-size: 13px;
  color: #3f404a;
}
.form-control {
  background: none;
  border: 1px solid #e4e6ef;
}

label {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #a4a5b2;
}

i {
  position: relative;
  top: -32px;
  padding-right: 10px;
  float: right;
  color: #afb0bc;
}

i.btc {
  position: relative;
  top: -32px;
  padding-right: 30px;
  float: right;
}

.select {
  margin-top: 30px;
  width: 210px;
  height: 41px;
  font-style: normal;
  font-weight: 700;
  font-size: 13px;
  color: #000;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border: none;
}

.buy-btn {
  background: #06ca6b;
}

.sell-btn {
  background-color: red;
}

input {
  box-shadow: none !important;
}

@media only screen and (max-width: 500px) {
  .sell-gp {
    display: flex;
    flex-direction: column;
  }

  .buy {
    display: flex;
    flex-direction: column;
  }

  .sell {
    display: flex;
    flex-direction: column;
  }
}
</style>
