<template>
    <header>
        <h1>ANDREW<span>MAHE</span></h1>
        <a href="" class="transition">Un café ? ☕</a>
    </header>
</template>
  
<style scoped>

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

header a{
    text-decoration: none;
    color: var(--white);
    font-family: var(--medium);
    font-weight: 900;
    text-transform: uppercase;
    font-size: 20px;
    padding: 10px 30px;
    color: var(--yellow);
    outline: solid 1.5px var(--yellow);
    border-radius: 20px;
    overflow: hidden;
}

header a:hover{
    color: var(--blue);
}

header a:after {
    content: '';
    width: 300px;
    height: 300px;
    position: absolute;
    left: 0;
    top: 0;
    z-index: -1;
    background-color: var(--yellow);
    transition: all .5s ease-in-out;
    -webkit-transition: all .5s ease-in-out;
    -webkit-transform: translateX(-100%) translateY(0%) rotate(45deg);
    transform: translateX(-100%) translateY(0%) rotate(45deg);
}

header a:hover:after{
    -webkit-transform: translateX(-2%) translateY(-25%) rotate(45deg);
    transform: translateX(-2%) translateY(-25%) rotate(45deg);
}

/** Tablette **/
@media screen and (max-width: 1024px)  {
    
}

/** Tablette **/
@media screen and (max-width: 768px)  {
    header h1{
        font-size: 20px;
    }

    header h1 span{
        font-size: 21px;
    }

    header a{
        font-size: 20px;
        padding: 10px 30px;
        border-radius: 10px;
    }
}

</style>
  