<script setup lang="ts">
    import ImageLeftSection from '@/components/templates/ImageLeftSection.vue';
    import ImageRightSection from '@/components/templates/ImageRightSection.vue';
    import UXUIDesign from '@/components/images/UXUIDesign.vue';
    import Maintenance from '@/components/images/Maintenance.vue';
    import ListTypeSection from '@/components/templates/ListTypeSection.vue'; 
    import Formation from '@/components/images/Formation.vue';
    import Website from '@/components/images/Website.vue'; 
</script>

<template>

    <section>
        <h2>De quoi avez-vous besoin ?</h2>
        <p>
            Je prends plaisir à mettre mes compétences au service d'autrui. Je suis avant tout au service et à l'écoute 
            de mes clients, pour les aider à réaliser efficacement leurs projets web afin de faire de
             notre collaboration une réussite. Mes valeurs sont l'excellence, la transparence et la confiance.
        </p>

        <ImageLeftSection>
            <template #image><UXUIDesign></UXUIDesign></template>
            <template #title>UX & UI Design</template>

            <template #description>Lorem ipsum dolor sit amet, consectetur adipiscing 
                elit. Donec pharetra convallis velit eget lobortis. 
                Phasellus a sollicitudin justo, non pharetra neque. 
                Nullam mauris ipsum, volutpat ut risus eget, 
                vehicula facilisis enim.
            </template>

            <template #first_element><ListTypeSection></ListTypeSection> Élément</template>
            <template #second_element><ListTypeSection></ListTypeSection> Élément</template>
            <template #third_element><ListTypeSection></ListTypeSection> Élément</template>
            <template #fourth_element><ListTypeSection></ListTypeSection> Élément</template>
        </ImageLeftSection>

        <ImageRightSection>
            <template #image><Website></Website></template>
            <template #title>Création et refonte de votre site internet</template>

            <template #description>Lorem ipsum dolor sit amet, consectetur adipiscing 
                elit. Donec pharetra convallis velit eget lobortis. 
                Phasellus a sollicitudin justo, non pharetra neque. 
                Nullam mauris ipsum, volutpat ut risus eget, 
                vehicula facilisis enim.
            </template>

            <template #first_element><ListTypeSection></ListTypeSection>Élément</template>
            <template #second_element><ListTypeSection></ListTypeSection>Élément</template>
        </ImageRightSection>

        <ImageLeftSection>
            <template #image><Maintenance></Maintenance></template>
            <template #title>Maintenance de votre site internet</template>

            <template #description>Lorem ipsum dolor sit amet, consectetur adipiscing 
                elit. Donec pharetra convallis velit eget lobortis. 
                Phasellus a sollicitudin justo, non pharetra neque. 
                Nullam mauris ipsum, volutpat ut risus eget, 
                vehicula facilisis enim.
            </template>

            <template #first_element><ListTypeSection></ListTypeSection>Élément</template>
            <template #second_element><ListTypeSection></ListTypeSection>Élément</template>
        </ImageLeftSection>

        <ImageRightSection>
            <template #image><Formation></Formation></template>
            <template #title>Formation</template>

            <template #description>Lorem ipsum dolor sit amet, consectetur adipiscing 
                elit. Donec pharetra convallis velit eget lobortis. 
                Phasellus a sollicitudin justo, non pharetra neque. 
                Nullam mauris ipsum, volutpat ut risus eget, 
                vehicula facilisis enim.
            </template>

            <template #first_element><ListTypeSection></ListTypeSection>Élément</template>
            <template #second_element><ListTypeSection></ListTypeSection>Élément</template>
        </ImageRightSection>

    </section>

</template>
  
<style scoped> /* Local */

section{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    width: 75%;
    margin: auto;
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

/** Tablette **/
@media screen and (max-width: 1400px)  {
}

@media screen and (max-width: 1150px)  {
    
}

/** Tablette **/
@media screen and (max-width: 1024px)  {
}

/** Tablette **/
@media screen and (max-width: 768px)  {

}

</style>
  