<template>

<div class="checkbox">
  <div class="checkbox__result">
    {{arrNumbersResult}}
  </div>
  <div class="checkbox__list">
    <div  
    v-for="(item,id) in arrCheckbox"
    :key=id>
    <input class="checkbox__input" 
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

<style lang="scss">

@import '@/assets/style/checkbox.scss'

</style>