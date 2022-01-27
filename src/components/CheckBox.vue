<template>

<div class="checkbox">
  <div class="checkbox__result">
    {{arrNumbersResult}}
  </div>
  <div class="checkbox__list">
    <div  
    v-for="(item,id) in arrCheckbox"
    :key=id>
    <input class="checkbox__inpt" 
    type="checkbox"
    v-model="arrNumbers"
    :value="item.value">
    <h2 class="checkbox__value">
      {{item.value}}
    </h2>
    </div>
  </div>
</div>
 
</template>

<script>
export default {
    data(){
        return{
            arrNumbers:[],
            arrCheckbox:[
                {id:1,value:5},
                {id:2,value:8},
                {id:3,value:15},
                {id:4,value:22}
            ]
        }
    },
    computed: {
    arrNumbersResult: function () {
        return this.arrNumbers.map(parseFloat).reduce(function (sum,elem) {
            return sum + elem
            },0)
    }
  }
}
</script>

<style>
.checkbox{
    color: rgb(53, 53, 53);
}

.checkbox__list{
    display: flex;
    justify-content: center;
    margin-left: 45px;
}
.checkbox__inpt{
    display: block;
    margin-right: 50px;
    margin-bottom: 20px;
}
.checkbox__value{
    margin-top: -10px;
    margin-right: 10px;
}
.checkbox__result{
    display: block;
    margin: 0 auto;
    margin-bottom: 50px;
    width: 50px;
    height: 50px;
    border:1px solid black ;
    background: rgb(172, 250, 185);
    padding-bottom: 20px;
    font-size: 40px;
    text-align: center;
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