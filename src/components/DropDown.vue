<template>

 <div class="header__menu" >
   <nav class="side"> 
        <button class="menu__button"
         :class="{active:toggleActive}"
         @click="AddActive">
         <span></span>
        </button>
      <ul class="menu">
          <li class="menu__item"><a class="menu__link" href="#"><img src="/images/menuu.png" alt="menu">menu</a> 
            <ul class="menu__drop" >
              <li class="menu__item"><a class="menu__link" href="#">...</a></li>
              <li class="menu__item"><a class="menu__link" href="#">...</a></li>
            </ul>
        </li>
          <li class="menu__item"><a class="menu__link" href="#"><img src="/images/about.png" alt="about">about us</a>
          <ul class="menu__drop" >
              <li class="menu__item"><a class="menu__link" href="#">...</a></li>
              <li class="menu__item"><a class="menu__link" href="#">...</a></li>
          </ul>
        </li>
          <li class="menu__item"><a class="menu__link" href="#"><img src="/images/social.png" alt="social">contacts</a>
          <ul class="menu__drop" >
              <li class="menu__item"><a class="menu__link" href="#">...</a></li>
              <li class="menu__item"><a class="menu__link" href="#">...</a></li>
          </ul>
        </li>
      </ul>

     <ul class="menu-active"
     :class="{active:toggleActive}">
        <ul class="menu-active__item">
          <a class="menu-active__link" href="#" >menu</a>
          <li class="menu-active__sub-item"><a class="menu-active__link" href="#" >...</a></li>
          <li class="menu-active__sub-item"><a class="menu-active__link" href="#" >...</a></li>
        </ul>
        <ul class="menu-active__item">
          <a class="menu-active__link" href="#" >about</a>
          <li class="menu-active__sub-item"><a class="menu-active__link" href="#" >...</a></li>
          <li class="menu-active__sub-item"><a class="menu-active__link" href="#" >...</a></li>
         </ul>
        <ul class="menu-active__item">
          <a class="menu-active__link" href="#" >contacts</a>
          <li class="menu-active__sub-item"><a class="menu-active__link" href="#" >...</a></li>
          <li class="menu-active__sub-item"><a class="menu-active__link" href="#" >...</a></li>
        </ul>
     </ul>
    </nav> 
 </div>

</template>

<script>

export default {
    data(){
        return{
            toggleActive:true
        }
    },
    methods:{
        AddActive(){
            this.toggleActive = !this.toggleActive
        }
    }
}
</script>


<style lang="scss">

@import '@/assets/style/DropDown.scss' 

</style>