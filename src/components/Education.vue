<template>
    <div class="flex flex-col space-y-4 md:space-y-12 justify-center items-center">

        <EducationCard :info="{
        label: 'East West University(Bsc.)',
        desc: 'Major in Software Engineering',
        timeline: 'From January, 2017 to June 2021'
    }"
        :bgInfo="{
            margin: 'ml-16'
        }"
    />

    <EducationCard :info="{
        label: 'Cox\'s Bazar Govt. College(HSC)',
        desc: 'Major in Science',
        timeline: 'From January, 2013 to January 2015'
    }"
    
    :bgInfo="{
            
            margin: 'mr-16'
        }"
        />

    <EducationCard :info="{
        label: 'Cox\'s Bazar Govt. High School(SSC)',
        desc: 'Major in Science',
        timeline: 'From January, 2008 to January 2013'
    }"
    
    :bgInfo="{
            
            margin: 'ml-16'
        }"
        />

    </div>
</template>

<script>

import EducationCard from './sub_components/EducationCard.vue'

export default {
    components:{
        EducationCard,
    }
}
</script>

