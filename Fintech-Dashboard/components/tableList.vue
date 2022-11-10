<template>
  <div>
    <div class="list">
      <p class="name">{{ name }}</p>
      <p class="details date">{{ date }}</p>
      <p class="details address">{{ address }}</p>
      <p class="details phone">{{ phone }}</p>
      <button><img src="~/assets/button.png" alt="" /></button>
    </div>

    <hr />
  </div>
</template>

<script>
export default {
  props: ["name", "date", "address", "phone"],
};
</script>

<style scoped>
.list {
  display: flex;
  justify-content: space-between;
  margin-top: 25px;
}

p {
  display: flex;
  justify-content: flex-start;
  text-align: left;
}

p.name {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #3f404a;
}

p.details {
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #a4a5b2;
}

p.name {
  width: 250px;
}

.date {
  width: 270px;
}

.address {
  width: 270px;
}

.phone {
  width: 200px;
}

button {
  background: none;
  border: none;
}

@media only screen and (max-width: 500px) {
  button {
    display: none;
  }

  .address {
    margin-left: -30px;
  }
}
</style>
