<script setup lang="ts">

    import PresentationIconVue from './icons/PresentationIcon.vue';

</script>

<template>
    
    <section>
        <div class="left">
            <h1>Développeur Web & Formateur à Caen</h1>
            <p> Lorem ipsum dolor sit amet, consectetur 
                adipiscing elit. Pellentesque sit amet metus 
                ut sapien luctus accumsan eu ac enim.
            </p>
            <a href="#">En savoir plus</a>
        </div>

        <div class="right">
            <PresentationIconVue></PresentationIconVue>
        </div>
    </section>

</template>
  
<style scoped>

section{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    height: 70vh;
}

section .left{
    margin: 0 50px 0 0;
}

section .left h1{
    font-family: var(--bold);
    font-size: 4em;
    line-height: 100%;
    letter-spacing: -2px;
    margin-bottom: 20px;
}

section .left p{
    font-weight: 300;
    font-size: 1.5em;
    line-height: 175%;
    margin-bottom: 20px;
    font-family: var(--light);
}

section .left a{
    color: var(--yellow);
    text-decoration: none;
    font-size: 1.5em;
    font-family: var(--bold);
    padding-left: 50px;
}

section .left a:before{
    content: '';
    width: 25px ;
    height: 2px;
    background-color: var(--yellow);
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    margin: auto 0;
}

/** Tablette **/
@media screen and (max-width: 1024px)  {
    section{
        flex-direction: column;
        height: initial;
    }
}

/** Tablette **/
@media screen and (max-width: 768px)  {
    
}

</style>
  