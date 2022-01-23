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
body{
  background-image: url('/images/qqqq.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  margin: 0;
  box-sizing: border-box;
}
.header{
  width: 100%;
  background-image: url('/images/m.jpg');
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
  margin-left: 110px;
}
@media (max-width:600px) {
  .header{
    padding-top:40px ;
  }
  .header__inpt{
    width: 200px;
    height: 30px;
    margin-left: 80px;
  }
  .logo{
    position: absolute;
    top:40px;
    right: 50px;
    margin-left: 70px;
  }
}
@media (max-width: 400px) {
  .header__inpt{
    width: 150px;
    height: 30px;
    margin-left: 60px;
  }

    }
@media (max-width:360px) {
  .header__inpt{
    width: 130px;
    height: 30px;
    margin-left: 50px;
  }

}

</style>


