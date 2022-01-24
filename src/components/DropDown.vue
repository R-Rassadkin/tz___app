<template>
 <div >
    <nav class="side"> 
         <button class="menu__btn"
          :class="{active:activeClassMenu}"
          @click="AddActive">
             <span></span>
         </button>
      <ul class="menu">
          <li class="menu__link"><a class="menu__link" href="#"><img src="/images/menuu.png" alt="menu">menu</a> 
            <ul class="menu__drop" >
              <li><a href="#">catalog</a></li>
              <li><a href="#">catalog</a></li>
            </ul>
        </li>
        <li ><a class="menu__link"><img src="/images/about.png" alt="menu">about us</a>
          <ul class="menu__drop" >
              <li><a href="#">about</a></li>
              <li><a href="#">abot</a></li>
          </ul>
        </li>
        <li><a class="menu__link" href="#"><img src="/images/social.png" alt="menu">contacts</a>
          <ul class="menu__drop" >
              <li><a href="#">adress</a></li>
              <li><a href="#">adress</a></li>
          </ul>
        </li>
      </ul>
     <ul class="menu-active"
     :class="{active:activeClassMenu}">
         <li class="menu-active__item"><a href="#" >menu</a></li>
         <li class="menu-active__sub-item"><a href="#" >...</a></li>
         <li class="menu-active__sub-item"><a href="#" >...</a></li>
         <li class="menu-active__item"><a href="#" >about</a></li>
         <li class="menu-active__sub-item"><a href="#" >...</a></li>
         <li class="menu-active__sub-item"><a href="#" >...</a></li>
         <li class="menu-active__item"><a href="#" >contacts</a></li>
         <li class="menu-active__sub-item"><a href="#" >...</a></li>
         <li class="menu-active__sub-item"><a href="#" >...</a></li>
     </ul>
    </nav> 
 </div>
</template>

<script>

export default {
    data(){
        return{
            activeClassMenu:false
        }
    },
    methods:{
        AddActive(){
            this.activeClassMenu = !this.activeClassMenu
        }
    }
}
</script>

<style>
ul li{
    list-style-type: none;
}


.menu{
    display: flex;
    margin-left: 100px;
    color: white;
}
.menu__drop{
    position: absolute;
    left: 0;
    width: 100%;
    display: none;
    padding: 0;
    
}
.menu li{
    display:inline-block;
    width: 100%;
    list-style-type: none;
    background: rgb(50, 54, 50);
    position: relative;
}
 .menu a{
    font-size: 40px;
    color: rgb(255, 255, 255);
    text-decoration: none;
    display: block;
    text-align: center;
    padding: 0 10px;
    line-height: 40px;
    transition: all .5s;
    cursor: pointer;
    z-index: 10;
}
.menu a:hover{
    background-color: rgb(28, 122, 28);
    z-index: 10;
}

.menu li:hover ul{
    display: block;
}
.menu__list::before{
    content:url("/images/arrow.svg");
    
margin-right: 10px;
}
.menu__btn{
    display: none;
} 

/* mobile menu */
.menu-active{
    position: absolute;
    top:80px;
    right: 0;
    width: 100%;
    background-color: rgb(79, 172, 63);
    display: block;
    transition: all 0.5s;
    height: 1700px;
    text-align: left;
    
}
.menu-active__item{
    list-style-type: none;
    
}
.menu-active__sub-item{
    margin-left: 20px;
}
.menu-active a{
    text-align: left;
    text-decoration: none;
    color: rgb(5, 5, 5);
    font-size: 90px;
    border-bottom: 3px solid rgb(207, 201, 201);
    font-weight: 900;
    margin-left: 10px;
}
.menu-active.active{
    transform: translate(-500%);
}



@media  (max-width:600px) {
    .menu-active{
        top: 127px;
    }
    .menu__btn {
        display:inline-block;
        width: 30px;
        height: 30px;
        border: none;
        padding: 0;
        position: absolute;
        background-color: transparent;
        top: 40px;
        left: 20px;
        }
        .menu__btn::before,
        .menu__btn::after{
            content: '';
            position: absolute;
            width: 100%;
            left: 0;
            height: 3px;
            background-color: white;
        }
        .menu__btn::before{
            top: 0;
        }
        .menu__btn::after{
            bottom: 0;
        }

        .menu__btn span{
            display: block;
            height: 3px;
            background-color: white;
        }
        .menu {
            transform: translate(-300%);
        }
}
@media  (max-width:400px) {
    .menu-active{
        top: 77px;
    }
}
@media  (max-width:810px) {
    .menu a{
        font-size: 15px;
    }
}

</style>