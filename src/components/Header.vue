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

        methods: {
            displayMenu() {
                this.showMenu = !this.showMenu;
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

        <!-- Menu portable -->
        <div class="hamburgerMenuContainer" @click="displayMenu()" :class="{ active: showMenu }">
            <span></span>
            <span></span>
            <span></span>
        </div>
            
    </header>
</template>
  
<style>

header{
    padding: 44px 0px;
    display: flex;
    justify-content: space-between;
    align-items: center;
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

.hamburgerMenuContainer.active::before{
    
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

header .contact{
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

header .contact:hover{
    color: var(--blue);
}

 header .contact:after {
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

header a:hover:after{
    -webkit-transform: translateX(-2%) translateY(-30%) rotate(45deg);
    transform: translateX(-2%) translateY(-30%) rotate(45deg);
} 



/** Tablette **/
@media screen and (max-width: 1024px)  {

    .computerMenu{
        display: none;
    }

    .hamburgerMenuContainer{
        display: initial;
        position: relative;
        /* background-color: red; */
        left: -15px;
    }

    .hamburgerMenuContainer::before{
        content: '';
        position:absolute;
        width:30px;
        height:30px;
        border: solid var(--white) 1px;
        rotate: 45deg;
        top: -9px;
        left: -10px;
        transition: 0.25s ease-in-out;
        cursor: pointer;
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
        transition: 0.25s ease-in-out;
        display: block;
        width: 20px;
        height: 1px;
        margin-bottom: 5px;
        position: relative;
        left: -5px;
        background: var(--white);
        z-index: 1;
        transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
                    background 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
                    opacity 0.55s ease;
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
    header h1{
        font-size: 20px;
    }

    header h1 span{
        font-size: 21px;
    }

    header .contact{
        font-size: 20px;
        padding: 10px 30px;
        border-radius: 10px;
    }
}

</style>
  