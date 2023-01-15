

<template>
    <img alt="Photo d'Andrew Mahé" src='@/assets/images/andrew.jpg' class="transition" />
</template>
  
   
  <style scoped>
  
  img{
    max-width: 350px;
    max-height: 600px;
    height: auto;
    border: var(--white) 2.5px solid;
    margin: 0 25px;
  }
  
  
  /** Tablette **/
  @media screen and (max-width: 1024px)  {
    img{
      max-width: 300px;
      margin: 0 0 25px 0;
    }
      
  }
  
  /** Tablette **/
  @media screen and (max-width: 768px)  {
    img{
      max-width: 275px;
      max-height: 500px;
      margin: 0 0 25px 0;
    }
  }
  
  </style>