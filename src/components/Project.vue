<script lang="ts">
import StepProject from './templates/step-project.vue';

export default({
        components: {
            StepProject
        },

        data() {
            return {
                nbImages: 5,
            }
        },

        
        created () {
            window.addEventListener('scroll', this.animateIfInView);
        },
        unmounted () {
            window.removeEventListener('scroll', this.animateIfInView);
        },

        methods: {
            animateIfInView () {
                const fadeList = document.getElementsByClassName('fade');

                for (var i = 0; i < fadeList.length; ++i) {
                    var item = fadeList[i];  
                    if(this.isElementInViewport(fadeList[i])){
                        item.classList.add('inView');
                    } else {
                        item.classList.remove('inView');
                    }
                }
            },

            isElementInViewport(el: any){
                var rect = el.getBoundingClientRect();

                if(window.innerWidth < 800){
                    return (
                        rect.top >= 0 &&
                        rect.left >= 0 &&
                        rect.bottom <= window.innerHeight * 1.15   &&
                        rect.right <= window.innerWidth * 1 
                    );
                }

                return (
                    rect.top >= 0 &&
                    rect.left >= 0 &&
                    rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
                    rect.right <= (window.innerWidth || document.documentElement.clientWidth) 
                );
            }
        },
        
    });


</script>

<template>
    <section class="transition">
        <h2>Déroulement de la création de votre site</h2>

        <StepProject class="fade">
            <template #step_numero>01</template>
            <template #step_title>Le devis et cahier des charges</template>
            <template #step_description>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit elementum lacinia. Donec quis molestie nibh. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna, sed blandit sem facilisis non. Curabitur libero velit, dignissim eu vestibulum a</template>
        </StepProject>
        <StepProject class="fade">
            <template #step_numero>02</template>
            <template #step_title>Le wireframe</template>
            <template #step_description>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit elementum lacinia. Donec quis molestie nibh. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna, sed blandit sem facilisis non. Curabitur libero velit, dignissim eu vestibulum a</template>
        </StepProject>
        <StepProject class="fade">
            <template #step_numero>03</template>
            <template #step_title>Maquette et prototype interactif</template>
            <template #step_description>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit elementum lacinia. Donec quis molestie nibh. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna, sed blandit sem facilisis non. Curabitur libero velit, dignissim eu vestibulum a</template>
        </StepProject>
        <StepProject class="fade">
            <template #step_numero>04</template>
            <template #step_title>Développement</template>
            <template #step_description>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit elementum lacinia. Donec quis molestie nibh. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna, sed blandit sem facilisis non. Curabitur libero velit, dignissim eu vestibulum a</template>
        </StepProject>
        <StepProject class="fade">
            <template #step_numero>05</template>
            <template #step_title>Mise en ligne</template>
            <template #step_description>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit elementum lacinia. Donec quis molestie nibh. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna, sed blandit sem facilisis non. Curabitur libero velit, dignissim eu vestibulum a</template>
        </StepProject>
        <StepProject class="fade" id="step__last">
            <template #step_numero>06</template>
            <template #step_title>Formation</template>
            <template #step_description>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis blandit elementum lacinia. Donec quis molestie nibh. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla dictum euismod magna, sed blandit sem facilisis non. Curabitur libero velit, dignissim eu vestibulum a</template>
        </StepProject>

    </section>
</template>
  
<style scoped> /* Local */
    section{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        text-align: center;
        width: 80%;
        margin: auto;
        color: var(--white);
    }

    section h2{
        font-size: 60px;
        font-family: var(--bold);
        margin-bottom: 175px;
    }

    .fade {
        opacity: 0;
        -webkit-transform: translate(0,50px);
        -moz-transform: translate(0,50px);
        -ms-transform: translate(0,50px);
        transform: translate(0,50px);
        -webkit-transition: opacity .6s .1s,transform .6s ease;
        transition: opacity .6s .1s,transform .6s ease;
        transition-delay: 0ms;
    }

    .inView {
        opacity: 1!important;
        -webkit-transform: translate(0,0)!important;
        -moz-transform: translate(0,0)!important;
        -ms-transform: translate(0,0)!important;
        transform: translate(0,0)!important;
    }

    /** Tablette **/
    @media screen and (max-width: 1400px)  {
        section{
            width: 90%;
        }
    }

    @media screen and (max-width: 1150px)  {


        
    }

    /** Tablette **/
    @media screen and (max-width: 1024px)  {
        section h2{
            font-size: 40px;
            margin-bottom: 75px;
        }
    }

    /** Tablette **/
    @media screen and (max-width: 768px)  {

    }

</style>
  