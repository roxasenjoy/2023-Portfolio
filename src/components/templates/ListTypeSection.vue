

<template>
    <div class="list_rectangle_outside">
        <div class="list_rectangle_inside"></div>
    </div>
</template>
  
   
<style scoped>
  
.list_rectangle_outside{
    width: 15px;
    height: 15px;
    border: 1px solid var(--white);
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
    margin: 0 10px 0 0;
}

.list_rectangle_inside{
    width: 7.5px;
    height: 7.5px;
    border: 1px solid var(--white);
    margin: auto;
    bottom: -22%;
}


/** Tablette **/
@media screen and (max-width: 1024px)  {

}

/** Tablette **/
@media screen and (max-width: 768px)  {

}
  
</style>