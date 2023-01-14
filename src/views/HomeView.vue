<script setup lang="ts">
      
  import SeparationSection from '../components/templates/SeparationSection.vue';
  import Header from '../components/Header.vue';
  import Presentation from '../components/Presentation.vue';
  import PersonnalInformation from '@/components/PersonnalInformation.vue';

</script>

<template>
    <Header></Header>
    <Presentation></Presentation>
    <SeparationSection></SeparationSection>

    <PersonnalInformation></PersonnalInformation>
    <SeparationSection></SeparationSection>
</template>