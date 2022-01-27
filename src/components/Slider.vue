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

<style >

.container{
  max-width: 1200px;
  margin: 0 auto;
}
.slider__wrapper{
  height: 500px;
  margin-bottom: 100px;
}
.slider__list{
  height: 100%;
  max-width: 700px;
  display: none;
  margin: 0 auto;
  padding-top: 50px;
}
.slider__btns{
  margin-top: 70px;
  display: block;
  text-align: center;
}
.slider__btn-next{
    padding: 0 103px;
    height: 30px;
    background-color: rgb(179, 243, 75);
    border: 1px solid black;
    font-weight: 700;
    border-radius:10px;
    align-items: center;
    display: inline-block;
    margin-bottom: 20px;
    margin-left: 20px;
    display: inline-block
}
.slider__btn-next:hover{
  background-color: rgb(221, 221, 95);
}
.slider__btn{
  display: none;
}
.slider__img{
  width: 100%;
}
.slide{
  display: none;
}
.active__slide{
  display: block;
}
.slide__itm{
  width: 100%;
}
@media (max-width: 600px) {
  .slider__btn-next{
    padding: 0 30px;
  }
  .slider__wrapper{
    height: 400px;
  }
}
@media (max-width: 500px) {
  .slider__wrapper{
    height: 300px;
  }
}
@media (max-width: 400px) {
  .slider__wrapper{
    height: 250px;
  }
}
@media (max-width: 300px) {
  .slider__wrapper{
    height: 190px;
  }
}
</style>