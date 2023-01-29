
<script setup lang="ts">
   
</script>

<!-- Création du template qui permet de mettre une photo à gauche et le texte à droite-->
<template>
    <div class="container">

        <slot name="image"></slot>
        <div class="content">
            <h3>
                <slot name="title"></slot>
            </h3>

            <p>
                <slot name="description"></slot>
            </p>

            <ul>
                <li>
                    
                    <slot name="first_element"></slot>
                </li>
                <li>
                    <slot name="second_element"></slot>
                </li>
                <li>
                    <slot name="third_element"></slot>
                </li>
                <li>
                    <slot name="fourth_element"></slot>
                </li>
            </ul>
        </div>
        
    </div>
</template>
  
   
<style scoped>

.container{
    display: flex;
    justify-content:space-evenly;
    align-items: center;
    flex-direction: row;
    width:100%;
    margin:50PX auto;
}

.container .content{
    text-align: left;
    margin-left: 30vh;
}

.container h3{
    font-size: 40px;
    font-family: var(--bold);
}

.container p{
    font-family: var(--light);
    line-height: 150%;
    font-size: 20px;
    margin: 15px 0 30px 0;
}

.container li{
    list-style: none;
    display: flex;
    flex-direction: row;
    align-items: center;
    margin: 10px 0;
    font-size: 20px;
    line-height: 150%;
}

/** Tablette **/
@media screen and (max-width: 1024px)  {
    
}

/** Tablette **/
@media screen and (max-width: 768px)  {

}
  
</style>