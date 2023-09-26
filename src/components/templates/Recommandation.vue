

<template>
    <div class="container__recommandation">
        <div class="top-text">
            <div  class="text__recommandation"><slot name="text"></slot></div>
        </div>
        <div class="bottom-text">
            <div class="container__client">
                <div class="client">
                    <p class="nameRecommandation"><slot name="name"></slot></p>
                    <p class="companyRecommandation"><slot name="company"></slot></p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>


.container__recommandation {
    width: 250px;
    height: 400px;
    border: solid 1.5px var(--white);
    font-family: var(--light);
    margin: 0 25px;
    position: relative;
    box-sizing: border-box;
    
}

.top-text, .bottom-text {
    width: 100%;
    text-align: center;
    padding: 25px;
}

.top-text {
    position: absolute;
    top: 10px;
    padding: 10px;
    text-align: left;
    font-size: 18px;
    line-height: 150%;
}

.bottom-text {
    position: absolute;
    bottom: 10px;
}

.containerText{
    position: absolute;
    top: 10px;
    padding: 25px;
}

.container__client{
    display: flex;
    justify-content: bottom;
    align-items: center;
    flex-direction: row;
    margin-top: 15px;
    text-align: left;
    position: absolute;
    bottom: 10px;
}

.text__recommandation{
    display: flex;
    vertical-align: top;
}

.image{
    background-color: var(--white);
    border-radius: 50%;
    height: 50px;
    width: 50px;
    margin-right: 15px;
}

.nameRecommandation{
    font-size: 16px;
    font-family: var(--bold);
    line-height: 150%;
}

.companyRecommandation{
    font-size: 14px;
    font-family: var(--light);
    line-height: 150%;
}

/** Tablette **/
@media screen and (max-width: 1024px)  {

}

/** Tablette **/
@media screen and (max-width: 768px)  {

}
  
</style>