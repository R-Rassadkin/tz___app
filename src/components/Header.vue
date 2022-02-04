<template>
   <header class="header">
     <div class="container">
       <div class="header__form">
        <img class="header__logo" src="@/assets/logo.svg" alt="logo">
        <div class="header__wrapper">
          <div class="header__input-wrapper">
            <input class="header__input" type="text" placeholder="строка поиска">
          </div>
         <DropDown></DropDown>
        </div>
       </div>
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

<style lang="scss">

@import '@/assets/style/Header.scss'

</style>


