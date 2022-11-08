<template>
  <div>
    <div class="heading">
      <div class="two">
        <div class="status" :class="color"></div>
        <p>{{ market }}</p>
      </div>
      <p class="percent" :class="color2">{{ percent }}</p>
    </div>

    <hr />
  </div>
</template>

<script>
export default {
  props: ["market", "percent", "color", "color2"],
};
</script>

<style scoped>
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 10px;
}

.two {
  display: flex;
  align-items: center;
}

.status {
  width: 7.3px;
  height: 7.3px;
  margin-top: -12px;
  background-color: #000;
  border-radius: 3.8px;
}

p {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #a4a5b2;
  margin-left: 8px;
  width: 205px;
}

.percent {
  margin-top: -10px;
  color: #000;
  display: flex;
  justify-content: flex-end;
  margin-top: 6px;
}

.pending {
  background: #d91a1a;
}

.pending1 {
  color: #d91a1a;
}

.complete {
  background: #06ca6b;
}

.complete1 {
  color: #06ca6b;
}
</style>
