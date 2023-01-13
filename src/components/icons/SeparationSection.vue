

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
    /* padding: 20px 25px; */
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
    margin: auto;
    margin: 50px auto auto auto;
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
    
}

/** Tablette **/
@media screen and (max-width: 768px)  {

}
  
</style>