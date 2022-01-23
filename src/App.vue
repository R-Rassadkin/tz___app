<template>
<div>
  <Header></Header>
  <Slider></Slider>
  <VueForm></VueForm>
  <footer>
    
      <div class="footer">
        <div class="container">
          <div class="footer__box">
            <p class="footer__text"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit ratione alias id voluptatem fugiat, iusto dolores eos distinctio consectetur tenetur. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus labore sit.</p>
            <p class="footer__text"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam nesciunt aliquam explicabo, quidem tenetur eum id magnam voluptatum ipsam numquam! Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus labore sit.</p>
            <p class="footer__text"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Animi velit placeat blanditiis expedita, fugiat cumque molestiae quos corrupti voluptate praesentium? Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus labore sit.</p>
          </div>
        </div>
      </div>
    
  </footer>
  
  
  

  
</div>
  
  
</template>

<script>

import Header from '@/components/Header.vue'
import Slider from '@/components/Slider.vue'
import VueForm from './components/VueForm.vue'



export default {
  name: 'App',
  components: {
    Header,
    Slider,
    VueForm
  }
}
</script>

<style>
body{
  height: 100%;

}
li ul{
  list-style-type: none;
  text-decoration: none;
}
.container{
  max-width: 1200px;
  padding: 0 20px;
  margin: 0 auto;
}
.footer__box{
  column-count: 3;
  column-gap: 46px;
  padding-bottom: 50px;
  margin-bottom: 44px;
}
.footer__text{
  font-weight: 900;
  color: white;
}
.footer{
  padding-top: 50px;
  background-color: rgb(37, 90, 37);
}
  @media (max-width: 767px) {
    .footer__box{
      display: flex;
      flex-direction: column
      
  
}


    }
</style>
