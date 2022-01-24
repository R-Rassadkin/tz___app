<template>
<div class="container">
    <div class="checkbox">
        <h2 class="checkbox__result">{{result}}</h2>
        <div class="checkbox__list">
            <h1 class="checkbox__number">5</h1><input class="checkbox__item" v-model="arrNumbers" type="checkbox" value=5 >
            <h1 class="checkbox__number">8</h1><input class="checkbox__item" v-model="arrNumbers" type="checkbox" value=8>
            <h1 class="checkbox__number">12</h1><input class="checkbox__item" v-model="arrNumbers" type="checkbox" value=12>
            <h1 class="checkbox__number">15</h1><input class="checkbox__item" v-model="arrNumbers" type="checkbox" value=15>
            <h1 class="checkbox__number">22</h1><input class="checkbox__item" v-model="arrNumbers" type="checkbox" value=22>
        </div>
        <div class="btn__centr">
            <button class="chekbox__btn" @click="rslt">result</button>
        </div>
       
      
      
    </div>
</div>

</template>
<script>
export default {
    data(){
        return{
            arrNumbers:[],
            result:'',
            
        }
    },
    methods:{
        rslt(){
            this.result=this.arrNumbers.map(parseFloat).reduce(function (sum,elem) {
            return sum + elem
            },0)
        }
    }
}
</script>

<style>

.checkbox{
    display: block;
    margin: 0 auto;
    text-align: center;
    
}
.checkbox__result{
    display: block;
    text-align: center;
    margin: 0 auto;
    width: 50px;
    height: 50px;
    border:1px solid black ;
    background: rgb(172, 250, 185);
    margin-bottom: 20px;
    padding-top: 10px;
    font-size: 40px;
}
.checkbox__list{
    display: flex;
    justify-content: center;
    align-items: center;
}
.checkbox__item{
    margin-right: 50px;
}
.checkbox__number{
    margin-top: -10px;
    margin-right: 10px;
}
.chekbox__btn{
    
    height: 30px;
    background-color: rgb(116, 238, 100);
    border: 1px solid black;
    font-weight: 700;
    border-radius:10px;
    align-items: center;
    display: inline-block;
    width: 100px;
}



    @media (max-width:600px) {
        .checkbox__number{
    margin-top: -10px;
    margin-right: 5px;
        }
        .checkbox__item{
    margin-right: 10px;
}

    }

</style>