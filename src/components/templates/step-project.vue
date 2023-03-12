<template>

    <section class="step__container">
        <div class="left__container">
            <div class="step__squareContrainer">
                <div class="step__square">
                    <p><slot name="step_numero"></slot></p>
                </div>
            </div>
        </div>

        <div class="right__container">
            <h3 id="step_title"><slot name="step_title"></slot></h3>
            <p id="step_description"><slot name="step_description"></slot> </p>
        </div>
      
    </section>

</template>

<style scoped>

.step__container{
    display: flex;
    justify-content: space-evenly;
    align-items: flex-start;
    flex-direction: row;
    margin-bottom: 160px;
}

.right__container{
    width: 65%;
    margin-left:auto;
}

#step_title{
    font-family: var(--bold);
    font-size: 40px;
    text-align: left;
    margin-bottom: 25px;
}

#step_description{
    font-family: var(--light);
    font-size: 20px;
    text-align: left;
    line-height: 150%;
}

.step__square{
    border: solid white 1px;
    rotate: 45deg;
    width: 150px;
    height: 150px;
}

.step__square p:first-child{
    font-size: 80px;
    font-family: var(--bold);
    text-align: center;
    rotate: -45deg;
    left: -5px;
    bottom: -25px;
}

/** Tablette **/
@media screen and (max-width: 1400px)  {

}

@media screen and (max-width: 1150px)  {


    
}

/** Tablette **/
@media screen and (max-width: 1024px)  {
    #step_title{
        font-size: 30px;
    }

    .right__container{
        width: 75%;
        margin-left:auto;
    }

    #step_description{
        font-size: 18px;
    }

    .step__square{
        width: 75px;
        height: 75px;
    }

    .step__square p:first-child{
        font-size: 30px;
        left: 0px;
        bottom: -20px;
    }
}

/** Tablette **/
@media screen and (max-width: 600px)  {

    .step__square{
        width: 40px;
        height: 40px;
    }

    .step__square p:first-child{
        font-size: 20px;
        left: 0px;
        bottom: -6px;
    }
}

</style>