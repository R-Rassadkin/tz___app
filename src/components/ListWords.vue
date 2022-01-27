<template>
 <div class="select">
    <div class="select__btns">
      <button class="select__btn-clear" 
      @click="clear">clear
      </button>
      <button class="select__btn-sorting" 
      @click="btnSplit">sorting
      </button>
    </div>
    <input class="select__inpt" type="text" 
    v-model="str">
    <div class="select__reslt"  
    v-for="(item,idx) in arr" 
    :key="idx" >
    {{item}}
    </div>
</div>

</template>

<script>

export default {
    data(){
        return{
            str:'',
            arr:[],
        }
    },
    methods:{
        btnSplit(){ 
           this.arr=this.str.split(',').sort()
           this.arr.length=10
        },
        clear(){
            this.arr.length=0
            this.str=''
        }
    },
}
</script>

<style>


.select{
    display:block;
    text-align:center;
    background: rgb(124, 195, 130);
    width: 300px;
    margin: 0 auto;
    height: 350px;
    padding-top: 30px;
    border-radius: 20px;
    margin-top: 100px;
    margin-bottom: 30px;
}
.select__reslt{
    background: rgb(164, 241, 154);
    display: block;
    width: 245px;
    margin: 0 auto;
    border: 1px solid black;
    
}
.select__reslt li{
    list-style-type: none;
    display: block;
    width: 300px;
}
.select__btns{
    display: flex;
    justify-content: space-around;
}
.select__btn-sorting{
    padding: 0 30px;
    height: 30px;
    background-color: rgb(116, 238, 100);
    border: 0.5px solid black;
    font-weight: 700;
    border-radius:10px;
    align-items: center;
    display: inline-block;
    margin-left: 30px;
}
.select__btn-clear{
    padding: 0 37px;
    height: 30px;
    background-color: rgb(202, 114, 73);
    border: 1px solid black;
    font-weight: 700;
    border-radius:10px;
    align-items: center;
    display: inline-block;
    margin-bottom: 20px;
}
.select__inpt{
    display: block;
    margin: 0 auto;
    width: 245px;
}
@media (max-width: 400px) {
    .select{
    width: 280px;
    }
}

</style>