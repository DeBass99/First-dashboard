<template>
    <div>

        <div class="head">

            <div class="name">
                <h6> TECHNOLOGY </h6>
            </div>

            <div class="date">
                <p> updated at <strong> on Jan 23 </strong></p>
            </div>

        </div>

        <div class="roi">
            <h2> 27.24 <mark> ROI </mark> </h2>
        </div>

        <div class="graph-2">
            <img src="~/assets/graph 2.png" alt="">
        </div>

        <div class="list">
            <div class="item">  <div class="wrap"> <div class="high all"></div>  <p class="title"> Cloud Services </p> </div> <div class="percent"> <p>61%</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="mid all"></div>  <p class="title"> Automation </p> </div> <div class="percent"> <p>28%</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="low all"></div>  <p class="title"> Business Transformation </p> </div> <div class="percent"> <p>11%</p> </div> </div>
          </div>

    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

.head{ 
    display: flex;
    justify-content: space-between;
}

.head h3{ 
    font-style: normal;
    font-weight: 700;
    font-size: 13px;
    color: #3F404A;
}

.head p{ 
    font-style: italic;
    font-weight: 400;
    font-size: 12px;
    color: #A4A5B2;
}

.roi h2{ 
    font-style: normal;
    font-weight: 600;
    font-size: 19px;
    color: #3F404A;
}

mark{ 
    background: none;
    font-size: 14px;
    color: #A5A9C1;
}

.graph-2{ 
    text-align: center;
    margin-top: 12px;
}

.list{ 
    margin-top: 42px;
}

.wrap{ 
    display: flex;
    justify-content: flex-start;
    align-items: center;
}

.item{ 
    display: flex;
    justify-content: space-between;
}

.all{ 
    width: 8px;
    height: 8px;
    border-radius: 4px;
}

.high{ 
    background: #000AFF;
}

.mid{ 
    background: rgba(0, 71, 255, 0.5);
}

.low{ 
    background: #A4A5B2;
    opacity: 0.2;
}
p.title{ 
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    color: #3F404A;
    margin-left: 14px;
    margin-bottom: 0px;
}

.percent p{ 
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    color: #A4A5B2;
}

img{ 
    width: 100%;
}


</style>