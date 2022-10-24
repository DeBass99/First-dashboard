<template>
  <div class="app"> 

    <b-row class="top-name">

      <b-col class="top-text" md="3">

        <div class="all-stuffs">

        <div class="head">
          <p class="heading"> INVESTMENT SECTORS </p>
        </div> 

        <div class="text">
          <One />
        </div>

      </div>

      <div class="vertical"></div>

      </b-col>


      <b-col class="top-text" md="3">

      <div class="all-stuffs">

      <div class="head">
        <p class="heading"> TECH PERFORMANCE </p>
      </div> 

      <div class="text">
        <Two />
      </div>

      </div>

      <div class="vertical"></div>

      </b-col>


      <b-col class="top-text" md="3">

      <div class="all-stuffs">

      <div class="head">
        <p class="heading"> HLTH PERFORMANCE </p>
      </div> 

      <div class="text">
        <Three />
      </div>

      </div>

      <div class="vertical"></div>

      </b-col>


      <b-col class="top-text" md="3">

      <div class="all-stuffs">

      <div class="head">
        <p class="heading"> AGENTS </p>
      </div> 

      <div class="text">
        <Four />
      </div>

      </div>

      </b-col>

    </b-row>

    <b-row>
      <b-col mb="12" class="overview">
        <div class="head-2">

          <p class="title"> OVERVIEW </p>

          <p class="date"> updated at <strong>7:01am on Jan 23</strong></p>

        </div>
      </b-col>
    </b-row>

    <b-row >
      <b-col md="12">

        <Table1 />

      </b-col>
    </b-row>

  </div>
</template>



<script>
import One from '../components/one.vue';
import Two from '../components/two.vue';
import Three from '../components/three.vue';
import Four from '../components/four.vue';
export default {
    name: "IndexPage",
    components: { One, Two, Three, Four }
}
</script>



<style scoped> 

  .top-name{ 
    margin-top: 30px;
  }

  .top-text{ 
    display: flex;
    justify-content: space-between;
    padding: 0px;
  }

  .all-stuffs{ 
    display: flex;
    flex-direction: column;
    flex: 0 0 99.5%;
  }

  .head{ 
    background: #F3F4F9;
  }

  .head p{ 
    padding: 20px 0px 20px 30px;
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    color: #A4A5B2;
  }

  .text{ 
    padding: 30px;
  }

  .vertical{  
            border-left: 2px solid #E2E3E9;
            height: 100%;
  }

  .overview{ 
    padding: 30px;
    background: #F3F4F9;
  }

.head-2{ 
  display: flex;
  justify-content: space-between;
}
p.title{ 
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  color: #A4A5B2;
}

p.date{ 
  font-style: italic;
  font-weight: 500;
  font-size: 12px;
  color: #A4A5B2;
}
  


</style>
