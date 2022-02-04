<template>

 <div class="slider">
  <div class="container">
    <div class="slider__list"
    :class="{active__slide: currentSlide === id}" 
    v-for="(item,id) in items"
    :key=id>
     <img  class="slide__itm"
     :src="item.src" alt="slide">
    </div>
    <div class="slider__btns">
      <button class="slider__btn-next" @click="prev">prev</button>
      <button class="slider__btn-next" @click="next">next</button>
    </div>
  </div>
 </div>

</template>
<script>
export default {
    data(){
        return{
          currentSlide:1,
          items:[
          {id:1,src:"/images/1.jpg"},
          {id:2,src:"/images/2.jpg"},
          {id:3,src:"/images/3.jpg"},
          {id:4,src:"/images/4.jpg"},
          {id:5,src:"/images/5.jpg"},
          ]
        }
    },
    methods:{
      next(){
      this.currentSlide===4 ? this.currentSlide=1 :this.currentSlide++
      console.log(this.currentSlide);
      },
      prev(){
        this.currentSlide===1 ? this.currentSlide=4 :this.currentSlide--
        }
    },
    // mounted(){
    //     setInterval(()=>{
    //         this.currentSlide===4 ? this.currentSlide=1 :this.currentSlide++
    //     },2000)
    // }
}
</script>

 



<style  lang="scss">

@import '@/assets/style/Slider.scss'

</style>