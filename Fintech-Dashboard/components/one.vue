<template>
    <div>

        <div class="graph-1">
            <p>Overview Status</p>
            <img src="~/assets/graph 1.png" alt="">
          </div>

          <div class="list">
            <div class="item">  <div class="wrap"> <div class="tech all"> <p>TECH</p> </div>  <p class="title"> Technology</p> </div> <div class="percent"> <p>26%</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="health all"> <p>HLTH</p> </div>  <p class="title"> Healthcare </p> </div> <div class="percent"> <p>9%</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="energy all"> <p>ENRG</p> </div>  <p class="title"> Energy </p> </div> <div class="percent"> <p>65%</p> </div> </div>
          </div>

    </div>
</template>

<script>
    export default {
        
    }
</script>

<style  scoped>

.graph-1{ 
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.graph-1 p{ 
    font-style: normal;
    font-weight: 700;
    font-size: 13px;
}

.list{ 
    margin-top: 30px;
}

.wrap{ 
    display: flex;
    justify-content: flex-start;
}

.item{ 
    display: flex;
    justify-content: space-between;
}

.all{ 
    width: 48px;
    height: 24px;
    border-radius: 47px;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    display: flex;
    justify-content: center;
}
.tech{ 
    background: rgba(0, 71, 255, 0.1);
    color: #000AFF;
}

.health{ 
    background: rgba(255, 0, 0, 0.25);
    color: #D91A1A;
}

.energy{ 
    background: #E2E3E9;
    color: #000;
}

p.title{ 
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    color: #3F404A;
    margin-left: 14px;
}

.percent p{ 
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    color: #A4A5B2;
}

</style>