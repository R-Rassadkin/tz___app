<template>
   <header class="header">
     <div class="container">
       <img class="logo" src="@/assets/logo.svg" alt="logo">
       <input class="header__inpt" type="text" placeholder="строка поиска">
       <DropDown></DropDown>
     </div>
   </header>
</template>

<script>

import DropDown from '@/components/DropDown.vue'

export default {
  name:'Header',

  components:{
    DropDown
  }
}
</script>

<style>
*{
  box-sizing: border-box;
}

body{
  background-image: url('/images/bg-img.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  margin: 0;
}
.header{
  height:155px;
  background-image: url('/images/header-sky.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  border-bottom: 3px solid rgb(90, 100, 88);
}
.container {
  max-width: 1120px;
  margin: 0 auto;
}
.header{
  padding-top: 20px;
}
.logo{
  margin-bottom: -60px;
}
.header__inpt{
  width: 400px;
  border-radius: 3px;
  border: 1px solid rgb(87, 87, 87);
  margin-left: 100px;
}
@media (max-width:600px) {
  .header{
    padding-top:40px ;
  }
  .header__inpt{
    width: 180px;
    height: 30px;
    margin-left: 80px;
  }
  .logo{
    position: absolute;
    top:30px;
    right: 50px;
    margin-left: 70px;
  }
  .header{
    height: 101px;
  }
}
@media (max-width: 400px) {
  .header__inpt{
    width: 150px;
    height: 30px;
    margin-left: 60px;
  }
  .header{
    height: 93px;
  }

}
@media (max-width:360px) {
  .header__inpt{
    width: 130px;
    height: 30px;
    margin-left: 50px;
  }
  .logo{
    right: 30px;
  }
}



</style>


