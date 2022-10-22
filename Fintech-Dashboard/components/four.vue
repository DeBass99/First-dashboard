<template>
    <div>

        <h3> Top Performers </h3>

        <div class="list">
            <div class="item">  <div class="wrap"> <div class="all"> <img src="~/assets/profile 1.png" alt=""> </div>  <p class="title"> Cloud Services </p> </div> <div class="price"> <p>£105,483</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="all"> <img src="~/assets/profile 2.png" alt=""> </div>  <p class="title"> Automation </p> </div> <div class="price"> <p>£16,788</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="all"> <img src="~/assets/profile 3.png" alt=""> </div>  <p class="title"> Business Transformation </p> </div> <div class="price"> <p>£66,881</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="all"> <img src="~/assets/profile 4.png" alt=""> </div>  <p class="title"> Business Transformation </p> </div> <div class="price"> <p>£7,538</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="all"> <img src="~/assets/profile 5.png" alt=""> </div>  <p class="title"> Business Transformation </p> </div> <div class="price"> <p>£8,942</p> </div> </div>
            <hr>
            <div class="item">  <div class="wrap"> <div class="all"> <img src="~/assets/profile 6.png" alt=""> </div>  <p class="title"> Business Transformation </p> </div> <div class="price"> <p>£1,004</p> </div> </div>
        </div>

    </div>
</template>

<script>
    export default {
        
    }
</script>

<style  scoped>

h3{ 
    font-style: normal;
    font-weight: 700;
    font-size: 13px;
    text-align: center;
    color: #3F404A;
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

.all img{ 
    width: 100%;
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

.price p{ 
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    color: #A4A5B2;
}

</style>