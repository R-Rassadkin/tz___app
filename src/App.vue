<template>
 <div>

  <Header></Header>
  <Slider></Slider>
  <VueForm></VueForm>
  <Footer></Footer>
  
 </div>

</template>

<script>
import Header from '@/components/Header.vue'
import Slider from '@/components/Slider.vue'
import VueForm from './components/VueForm.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header,
    Slider,
    VueForm,
    Footer
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

</style>
