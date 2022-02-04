<template>

 <div class="select">
    <div class="select__butons">
      <button class="select__buton-clear" 
      @click="clear">clear
      </button>
      <button class="select__buton-sorting" 
      @click="butonSplit">sorting
      </button>
    </div>
    <input  class="select__input" 
    type="text" 
    v-model="str">
    <div v-if="this.arr.length<10">
      <div class="select__result"
      v-for="(item,idx) in arr"
      :key="idx" >
      {{item}}
      </div>
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
        butonSplit(){
            this.arr=this.str.toLowerCase().split(',').sort();
            if (this.arr.length>10) {
               alert('Максимально кол-во слов:10')
            }
        },
        clear(){
            this.arr=[]
            this.str=''
        }
    }
}
</script>

<style lang="scss">

@import '@/assets/style/ListWords.scss'

</style>