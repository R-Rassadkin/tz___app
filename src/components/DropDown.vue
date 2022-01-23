
<template>
<div >
    <nav class="side"> 
         <button class="menu__btn"
          :class="{active:activeClassMenu}"
          @click="AddActive">
             <span></span>
         </button>
      <ul class="menu">
        <li><a class="menu__list" href="#">menu</a>
          <ul class="menu__drop" >
              <li class="deep"><a href="#">1</a></li>
              <li ><a href="#">2</a></li>
          </ul>
        </li>
        <li><a class="menu__list" href="#">about</a>
          <ul class="menu__drop" >
              <li class="deep"><a href="#">1</a></li>
              <li ><a href="#">2</a></li>
          </ul>
        </li>
        <li><a class="menu__list" href="#">conta</a>
          <ul class="menu__drop" >
              <li class="deep"><a href="#">1</a></li>
              <li><a href="#">2</a></li>
          </ul>
        </li>
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
           this.activeClassMenu?this.activeClassMenu=false:this.activeClassMenu=true
        }
    }

}
</script>

<style>



.menu{
    display: flex;
    margin-left: 20px;
    color: white;
}
.menu__drop{
    position: absolute;
    left: 0;
    width: 100%;
    display: block;
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
     font-size: 25px;
    color: rgb(255, 255, 255);
    text-decoration: none;
    display: block;
    text-align: center;
    padding: 0 10px;
    height: 40px;
    line-height: 40px;
    transition: all .5s;
    
}
.menu a:hover{
    background-color: rgb(99, 182, 99);
}

.menu li:hover ul{
    display: block;
}
.menu__list::before{
    content:url("/images/arrow.svg");
    
margin-right: 10px;
}
.menu__btn{
    
} 
/* .menu__btn.active{
    background-color: yellow;
} */

@media  (max-width:510px) {
    .menu{
        position: absolute;
        left: 0;
        display: block;
        margin-left: 0;
        padding: 0;
    }
    .menu a{
        
        width: 50px;
        font-size: 10px;
        
        
    }
    .menu__btn {
        display:inline-block;
        width: 30px;
        height: 30px;
        border: none;
        padding: 0;
        position: absolute;
        background-color: transparent;
        top: 23px;
        left: 10px;
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
        .menu li{
            width: 50px;
            width: 100%;

        }
        .menu__list{
            position: relative;
        }
        .menu__drop{
            position: absolute;
            width: 100%;
            left: 100%;
            top:0
        }
        .deep{
            width: 100%;
        }
        
     

    
}

</style>