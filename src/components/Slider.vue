<template>
<div class="slider">
  <div class="container">
    <div class="q">
      <div class="slider__list">
        <div v-if="currentSlide===1" class="slide">
          <img class="slider__img" src="/images/1.jpg" alt="img">
        </div>
        <div v-if="currentSlide===2" class="slide">
          <img class="slider__img" src="/images/2.jpg" alt="img">
        </div>
        <div v-if="currentSlide===3" class="slide">
          <img class="slider__img" src="/images/3.jpg" alt="img">
        </div>
        <div v-if="currentSlide===4" class="slide">
          <img class="slider__img" src="/images/4.jpg" alt="img">
        </div>
        <div v-if="currentSlide===5" class="slide">
          <img class="slider__img" src="/images/5.jpg" alt="img">
        </div>
    </div>
    

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
            currentSlide:1
        }
    },
    methods:{
      next(){
      this.currentSlide===5 ? this.currentSlide=1 :this.currentSlide++
      },
      prev(){
        this.currentSlide===1 ? this.currentSlide=5 :this.currentSlide--
        }
    },
    // mounted(){
    //     setInterval(()=>{
    //         this.currentSlide===5 ? this.currentSlide=1 :this.currentSlide++
    //     },7000)
    // }
}
</script>

<style >


.container{
  max-width: 1200px;
  margin: 0 auto;
}
.q{
  height: 500px;
  margin-bottom: 100px;
}
.slider__list{
  
  height: 100%;
  
  max-width: 700px;
  display: block;
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
@media (max-width: 600px) {
  .slider__btn-next{
    padding: 0 30px;
    
    
  }
 
  .q{
    height: 400px;
  }
  
}
@media (max-width: 500px) {
  .q{
    height: 300px;
  }
}
@media (max-width: 400px) {
  .q{
    height: 250px;
  }
}
@media (max-width: 300px) {
  .q{
    height: 190px;
  }
}




</style>