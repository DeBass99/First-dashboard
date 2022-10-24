<template>
    <div>

      <div class="head">
        <ul class="heading">
          <li> Name </li>
          <li> Date </li>
          <li> Address </li>
          <li> Phone </li>
          <li></li>
        </ul>

        <hr>
      </div>

      <tableList 
      v-for="(detail, i) in details"
      :key="i"
      :name="detail.name"
      :date="detail.date"
      :address="detail.address"
      :phone="detail.phone" />

    </div>
</template>

<script>
import json from "~/js/data.json"
    export default {
        data() {
          return {
            details: json,
          }
        },
    }
</script>

<style scoped>

ul.heading{ 
  list-style: none;
  display: flex;
  justify-content: space-between;
  margin-top: 10px;
  padding: 0px;
}

.heading li{ 
  display: flex;
  justify-content: flex-start;
  font-style: normal;
  font-weight: 500;
  font-size: 13px;
  color: #A4A5B2;

}

</style>