

<template>
    <div class="rectangle_outside">
        <div class="rectangle_inside"></div>
    </div>
</template>
  
   
<style scoped>
  
.rectangle_outside{
    width: 50px;
    height: 50px;
    border: 2px solid var(--white);
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
    margin: 30vh auto 30vh auto;
}

.rectangle_inside{
    width: 25px;
    height: 25px;
    border: 2px solid var(--white);
    margin: auto;
    bottom: -22.5%;
}


/** Tablette **/
@media screen and (max-width: 1024px)  {
    .rectangle_outside{
        margin: 20vh auto 20vh auto;
    }
}

/** Tablette **/
@media screen and (max-width: 768px)  {

}
  
</style>