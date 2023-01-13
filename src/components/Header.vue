<script lang="ts">

    declare interface Menu {
        showMenu: boolean,
    }

    export default {
        data(): Menu {
            return {
                showMenu: false
            }
        },

        mounted() {
            this.cancelScroll();
        },

        methods: {

            cancelScroll() {
                if(this.showMenu){
                    const scrollY = document.documentElement.style.getPropertyValue('--scroll-y');
                    const body = document.body;
                    body.style.height = '100vh';
                    body.style.overflowY = 'hidden';
                } else {
                    const body = document.body;
                    const scrollY = body.style.top;
                    body.style.position = '';
                    body.style.top = '';
                    body.style.height = '';
                    body.style.overflowY = '';
                    window.scrollTo(0, parseInt(scrollY || '0') * -1);
                }

                window.addEventListener('scroll', () => {
                        document.documentElement.style.setProperty('--scroll-y', `${window.scrollY}px`);
                    });
            },

            displayMenu(type: string) {

                if(type === 'menu' ||  ( this.showMenu && type === 'item')){
                    this.showMenu =!  this.showMenu;
                    this.cancelScroll();
                }
                
            }
        }
        
    }

</script>

<template>
    <header>
        <h1>ANDREW<span>MAHE</span></h1>
      
        <!-- Menu PC - Tablette-->
        <div class="computerMenu">
            <nav>
                <ul>
                    <a href=""><li>Services</li></a>
                    <a href=""><li>Portfolio</li></a>
                    <a href=""><li>Tarifs</li></a>
                    <a href=""><li>Fonctionnement</li></a>
                </ul>
            </nav>
            <a href="" class="transition contact">Un projet ?</a>
        </div>

        <!-- Icone hamburger -->
        <div class="hamburgerMenuContainer" @click="displayMenu('menu')" :class="{ active: showMenu }">
            <span id="hamburger1"></span>
            <span id="hamburger2"></span>
            <span id="hamburger3"></span>
        </div>    
    </header>

    <div class="nav" :class="{ active: showMenu }">
        <div class="nav__content">
            <ul class="nav__list">
                <a href="#"><li class="nav__list-item" @click="displayMenu('item')">Services</li></a>
                <a href="#"><li class="nav__list-item" @click="displayMenu('item')">Portfolio</li></a>
                <a href="#"><li class="nav__list-item" @click="displayMenu('item')">Tarifs</li></a>
                <a href="#"><li class="nav__list-item" @click="displayMenu('item')">Fonctionnement</li></a>
                <a href="#"><li class="nav__list-itemButton contact" @click="displayMenu('item')">Un projet ?</li></a>
            </ul>
        </div>
    </div>

</template>
  
<style scoped>

header{
    padding: 33px 0px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 100%;
    width: 75%;
    margin: auto;
}

header h1{
    font-family: var(--light);
    font-weight: 300;
    font-size: 30px;
}

header h1 span{
    font-size: 31px;
    font-family: var(--bold);
    font-weight: 300;
    line-height: 80.8%;
}

header div{
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
}

.hamburgerMenuContainer{
    display: none;
}

header nav ul{
    display: flex;
    list-style: none;
}

header nav ul a{
    text-decoration: none;
    color: white;
}

header nav ul li{
    padding: 5px 30px;
    text-align: center;
    font-family: var(--bold);
    display: flex;
    align-items: center;
    justify-content: center;
}

header .contact,
.nav .contact{
    text-decoration: none;
    font-family: var(--bold);
    font-weight: 900;
    text-transform: uppercase;
    font-size: 16px;
    padding: 10px 20px;
    color: var(--yellow);
    outline: solid 1.5px var(--yellow);
    border-radius: 5px;
    overflow: hidden;
}

header .contact:hover,
.nav__list-itemButton.contact:hover{
    color: var(--blue) !important;
}

header .contact:after,
.nav .contact:after {
    content: '';
    width: 500px;
    height: 500px;
    position: absolute;
    left: 0;
    top: 0;
    bottom: 50px;
    z-index: -1;
    background-color: var(--yellow);
    transition: all .75s ease-in-out;
    -webkit-transition: all .75s ease-in-out;
    -webkit-transform: translateX(-100%) translateY(0%) rotate(45deg);
    transform: translateX(-100%) translateY(0%) rotate(45deg);
}

header a:hover:after,
.nav .nav__list-itemButton:hover:after{
    -webkit-transform: translateX(-2%) translateY(-30%) rotate(45deg);
    transform: translateX(-2%) translateY(-30%) rotate(45deg);
} 

.nav {
    display: none;
}


/** Tablette **/
@media screen and (max-width: 1024px)  {

    header{
        max-width: 100%;
        width:90%;
    }

    /**
        Navigation qui arrive en slow motion pour rester sur toute la page
    */

    
 
    .nav {
        position: fixed;
        z-index: 1;
        top: 0;
        display: initial;
        overflow-y: hidden;
    }
    .nav:before, .nav:after {
        content: "";
        position: fixed;
        width: 100vw;
        height: 100vh;
        background: rgba(234, 234, 234, 0.2);
        z-index: -1;
        transition: transform cubic-bezier(0.77, 0, 0.175, 1) 0.8s;
        transform: translateX(0%) translateY(-100%);
    }
    .nav:after {
        background: var(--white);
        transition-delay: 0s;
    }
    .nav:before {
        transition-delay: 0.1s;
    }

    .nav.active{
        display: initial;
    }

     .nav__content {
        position: fixed;
        top: 50%;
        transform: translate(0%, -50%);
        width: 100%;
        text-align: center;
        font-size: 36px;
    }

    .nav__list-itemButton.contact{
        color: var(--yellow);
        font-size: 36px;
    }

    .nav__list{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    .nav__list-item,
    .nav__list-itemButton
     {
        position: relative;
        display: inline-block;
        transition-delay: 0.8s;
        opacity: 0;
        color: var(--blue);
        transform: translate(0%, 100%);
        transition: opacity 0.2s ease, transform 0.3s ease;
        margin: 25px 0;
        transform: scale(1);
    }
    .nav__list-item:after {
        background-color: currentColor;
        width: 30px;
        height: 1px;
        margin: 0 auto;
        left: 0;
        background-color: black;
        right: 0;
        top:100%;
        transform: scaleX(0);
        transition: all .2s ease;
        position: absolute;
        content: '';
    }

    .nav__list-item:hover:after{
        transform: scale(1.2);
        opacity: 1;
        width: 50%;
    }
    
    /**
        Menu ouvert
    */
    .nav.active {
        visibility: visible;
    }

    .nav a{
        cursor: default;
    }

    .nav.active{
        cursor: pointer;
    }

    .nav.active:before, .nav.active:after {
        transform: translateX(0%) translateY(0%);
    }

    .nav.active .nav__list-item,
    .nav.active .nav__list-itemButton {
        opacity: 1;
        transform: translateX(0%);
        transition: 0.3s ease-in-out;
    }

    /** Affichage smooth de tous les éléments de la navigation */
    

    .nav.active .nav__list-item:nth-child(0) {
        transition-delay: 0.5s;
    }
    .nav.active .nav__list-item:nth-child(1) {
        transition-delay: 0.6s;
    }
    .nav.active .nav__list-item:nth-child(2) {
        transition-delay: 0.7s;
    }
    .nav.active .nav__list-item:nth-child(3) {
        transition-delay: 0.8s;
    }
    .nav.active .nav__list-item:nth-child(4) {
        transition-delay: 0.9s;
    } 

    .nav.active .nav__list-itemButton:first-child{
        transition-delay: 0.5s;
    }

    .computerMenu{
        display: none;
    }

    .hamburgerMenuContainer{
        display: initial;
        position: absolute;
        z-index: 5;
        right: 15px;
    }

  

    .hamburgerMenuContainer::before{
        content: '';
        position:absolute;
        width:50px;
        height:50px;
        border: solid var(--white) 1px;
        rotate: 45deg;
        top: -16px;
        left: -16px;
        transition: 0.25s ease-in-out;
        cursor: pointer;
        z-index: 9999;
    }

    .hamburgerMenuContainer.active::before{
        border-color: var(--blue);
    }
    

    .hamburgerMenuContainer:hover::before{
        background-color: var(--white);
        transition: 0.25s ease-in-out;
    }

    .hamburgerMenuContainer:hover span{
        background: var(--blue);
        transition: 0.25s ease-in-out;
        cursor: pointer;
    }

    .hamburgerMenuContainer span
    {
        opacity: 1;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: .25s ease-in-out;
        -moz-transition: .25s ease-in-out;
        -o-transition: .25s ease-in-out;
        transition: 0.25s ease-in-out;
        display: block;
        width: 30px;
        height: 2px;
        margin-bottom: 5px;
        position: relative;
        left: -6.5px;
        background: var(--white);
        z-index: 9999;
        transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
                    background 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
                    opacity 0.55s ease;
    }

    .hamburgerMenuContainer.active #hamburger1{
        /* background-color: red; */ 
        transition: 0.25s ease;
        transform: translateX(4px) translateY(-1px) rotate(45deg);
    }

    .hamburgerMenuContainer.active #hamburger2{
        background-color: transparent;
        transform: translateX(10px);
        transition: 0.25s ease;
    }

    .hamburgerMenuContainer.active #hamburger3{
        /* background-color: green; */
        transition: 0.25s ease;
        transform: translateY(-6px) rotate(-45deg) translateX(-2px);
    }
    

    .hamburgerMenuContainer.active span{
        background: var(--blue);
    }

    .hamburgerMenuContainer span:last-child{
        margin-bottom: 0;
    }

    .hamburgerMenuContainer span:first-child
    {
    transform-origin: 0% 0%;
    }

    .hamburgerMenuContainer span:nth-last-child(2)
    {
        transform-origin: 0% 100%;
    }
}

/** Tablette **/
@media screen and (max-width: 768px)  {
    
}

</style>
  