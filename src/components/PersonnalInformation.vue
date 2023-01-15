<script setup lang="ts">
    import MoiImageVue from './images/MoiImage.vue';


</script>

<template>

    <section>
        <div class="left">
            <h2>Moi, c'est Andrew Mahé</h2>
            <p id="texte">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis aliquet augue 
                at sem lobortis pretium. Pellentesque ultricies, tortor id lacinia hendrerit,
                 ante leo tempor ante, id vulputate purus risus nec odio. Mauris ipsum urna, 
                 convallis et massa eu, pulvinar elementum urna.
            </p>

            <div class="stats">

                <div class="squareContainer">
                    <div class="square1 square">
                        <p>10</p>
                        <p>Projets <br/> réalisés</p>
                    </div>
                </div>
                
                <div class="squareContainer">
                    <div class="square2 square">
                    <p>4</p>
                    <p>Nombre de clients</p>
                    </div>
                </div>

                <div class="squareContainer">
                    <div class="square3 square">
                    <p>2</p>
                    <p>Années d'expériences</p>
                    </div>
                </div>
            </div>
        </div>

        

        <MoiImageVue></MoiImageVue>
    </section>

</template>
  
<style scoped> /* Local */
section{
    width: 75%;
    margin: auto;
    display: flex;
    justify-content:space-between;
    flex-direction: row;
    margin: 30vh auto 30vh auto;
}

.left{
    width: 70%;
    /* background-color: red; */
}

#texte{
    font-size: 26px ;
    font-family: var(--light);
    line-height: 175%;  
    margin: 0 0 100px 0
}

h2{
    font-size: 60px;
    font-family: var(--bold);
    margin-bottom: 25px;
}


.stats{
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 0px 0;    
}

.square{
    border: solid white 1px;
    rotate: 45deg;
    width: 150px;
    height: 150px;
}


.square p:first-child{
    font-size: 60px;
    font-family: var(--bold);
    text-align: center;
    rotate: -45deg;
    left: -20px;
    top: 20px;
}

.square p:nth-child(2){
    font-family: var(--light);
    font-size: 18px;
    text-align: center;
    rotate: -45deg;
    left: 15px;
    top: -5px;
}

/** Tablette **/
@media screen and (max-width: 1400px)  {
    section{
        width: 90%;
    }
}

@media screen and (max-width: 1150px)  {

    #texte{
        font-size: 18px;
    }

    .square{
        width: 125px;
        height: 125px;
    }

    .square p:first-child{
        font-size: 40px;
        left: -20px;
        top: 20px;
    }

    .square p:nth-child(2){
        font-family: var(--light);
        font-size: 16px;
        text-align: center;
        rotate: -45deg;
        left: 10px;
        top: 5px;
    }

    
}

/** Tablette **/
@media screen and (max-width: 1024px)  {
    section{
        width: 90%;
        flex-direction: column-reverse;
        justify-content: center;
        align-items: center;
        margin: 15vh auto 10vh auto;
    }

    .left{
        width:90%;
    }

    h2{
        font-size: 1.5em;
    }

    

    .square{
        margin: 35px 0;
    }

    #texte{
        margin: 0 0 25px 0;
    }
}

/** Tablette **/
@media screen and (max-width: 768px)  {

    .stats{
        flex-direction: column; 
    }
}

</style>
  