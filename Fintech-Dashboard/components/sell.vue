<template>
    <div class="app">
        <b-row class="all">
            <button class="choose buy-border2" @click="buyBtn2"> Buy </button>
            <button class="choose sell-border2" @click="sellBtn2"> Sell </button>

            <form action="submit" class="form">

          

            <div class="sell-gp" v-if="sell">
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
                <input type="text" class="form-control" aria-label="Amount (to the nearest dollar)">
                <i>$</i>
            </div>

            </b-col>

            <b-col class="sell">

                <div class="form-group">
                <label for="exampleFormControlSelect1">Amount</label>
                <select class="form-control input-style" id="exampleFormControlSelect1">
                <option>1</option>
                <option>2</option>
                <option>3</option>
                <option>4</option>
                <option>5</option>
                </select>
                <i class="btc">btc</i>
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
               <button class="select sell-btn"> SELL (PORTFOLIO) </button>
            </div>

            
            </b-col>
            </div>

            <div class="buy-gp" v-else>
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
                <input type="text" class="form-control" aria-label="Amount (to the nearest dollar)">
                <i>$</i>
            </div>

            </b-col>

            <b-col class="sell">

                <div class="form-group">
                <label for="exampleFormControlSelect1">Amount</label>
                <select class="form-control input-style" id="exampleFormControlSelect1">
                <option>1</option>
                <option>2</option>
                <option>3</option>
                <option>4</option>
                <option>5</option>
                </select>
                <i class="btc">btc</i>
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
               <button class="select buy-btn"> BUY (PORTFOLIO) </button>
            </div>

            
            </b-col>
            </div>

        </form>
        </b-row>
    </div>
</template>

<script>
import $ from "jquery";

    export default {
        data() {
            return {
            sell: true,
            }
        },

        methods: {
            buyBtn2(){
                this.sell = false
            $('.buy-border2' ).addClass("show-green2");
            $('.sell-border2' ).removeClass("show-red2");
            },

           sellBtn2(){
            this.sell = true;
            $('.sell-border2' ).addClass("show-red2"); 
            $('.buy-border2' ).removeClass("show-green2"); 
           },
    },
    mounted(){
        $('.sell-border2' ).addClass("show-red2");
    }
}
</script>

<style  scoped>
    .all{ 
        display: flex;
        justify-content: center;
    }

    .form-group{ 
        margin-top: 30px;
    }

    .buy-gp{ 
        display: flex;
        flex-direction: row;
    }

    .sell-gp{ 
        display: flex;
        flex-direction: row;
    }

    button.choose{ 
    padding: 12px 100px;
    background-color: #fff;
    border: 1px solid #E4E6EF;

    font-style: normal;
    font-weight: 400;
    font-size: 13px;
    color: #3F404A;
    }

    .show-green2{ 
        border-bottom: 5px solid #06CA6B!important;
    }

    .show-red2{ 
        border-bottom: 5px solid red!important;
    }

    .form-control{ 
    background: none;
    border: 1px solid #E4E6EF;
    }

    label{ 
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    color: #A4A5B2;

    }

    i{ 
        position: relative;
        top: -32px;
        padding-right: 10px;
        float: right;
        color: #AFB0BC;
    }

    i.btc{ 
        position: relative;
        top: -32px;
        padding-right: 30px;
        float: right;
    }

    .select{ 
        margin-top: 30px;
        width: 210px;
        height: 41px;
        font-style: normal;
        font-weight: 700;
        font-size: 13px;
        color: #FFFFFF;
        text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        border: none;
    }

    .buy-btn{ 
        background: #06CA6B;
    }

    .sell-btn{ 
        background-color: red;
    }

    input{ 
        box-shadow: none!important;;
    }


</style>