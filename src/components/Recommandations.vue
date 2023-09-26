<script setup lang="ts">

    import Recommandation from './templates/Recommandation.vue';

</script>

<template>
    
    <section>
        <h2>Faites comme eux ! <br> Choisissez mon expertise en développement</h2>
        <p>
            Je développe avec passion, et mes clients me tiennent toujours à coeur. C'est pourquoi nos relations sont si uniques lors du développement 
            de votre site Internet. Voici quelques-uns de ces retours d'éxperiences client.
        </p>

        <div class="recommandationsContainer">
            <Recommandation>
                <template #text>Je recommande vivement Andrew qui a su comprendre notre demande. Efficace, rapide et force de proposition. <br> 
                Nous continuerons notre collaboration avec Andrew.</template>
                <template #name>William BETHUS</template>
                <template #company> Les Cerises du Café</template>
            </Recommandation>

            <Recommandation>
                <template #text>Travail efficient, Andrew est à l’écoute et réactif.
Encore merci !</template>
                <template #name>Hugo TOUZE</template>
                <template #company>Aux caves des grands <br> cépages</template>
            </Recommandation>

        </div>

        

    </section>

</template>

<style scoped>

section{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    width: 75%;
    margin: auto;
    color: var(--white);
}

section h2{
    font-size: 60px;
    font-family: var(--bold);
}

section p{
    font-size: 20px;
    font-family: var(--light);
    line-height: 150%;
    margin: 25px 0 50px 0;
}

.recommandationsContainer{
    display: flex;
    justify-content: row;
}

/** Tablette **/
@media screen and (max-width: 1400px)  {
    section{
        width: 90%;
    }

    .container{
        margin: 50px auto 0 auto ;
    }
}

/** Tablette **/
@media screen and (max-width: 1024px)  {

    section h2{
        font-size: 40px;
    }

    section p{
        font-size: 18px;
    }

}

/** Tablette **/
@media screen and (max-width: 768px)  {

}

</style>
