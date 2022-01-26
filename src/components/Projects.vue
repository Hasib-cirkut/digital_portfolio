<template>

    <div class="w-2/3 m-auto">


        <div class="flex flex-col space-y-4">

            <div class="flex justify-center items-center space-y-4 md:space-x-4 flex-wrap md:flex-nowrap">
                <div>
                    <ProjectCard :info="{
                        label: 'remindme',
                        desc: 'A personalized to watch/read app that makes you a little bit less absentminded.'
                    }"
                    
                    
                    />
                </div>

                <div class="">
                    <ProjectCard :info="{
                        label: 'Personal Blog',
                        desc: 'Personal Blog using Creat React App and Contentful CMS.'
                    }"
                    
                    />
                </div>
            </div>

            <div class="flex justify-center items-center space-y-4 md:space-x-4 -mt-2 flex-wrap md:flex-nowrap">
                <div class="">
                    <ProjectCard :info="{
                        label: 'vote.com',
                        desc: 'A voting app based on nodejs/reactjs.'
                    }"
                    
                    
                    />
                </div>

                <div class="">
                    <ProjectCard :info="{
                        label: 'Disease Control Forum',
                        desc: 'A CRUD Forum dedicated to disease control and info sharing.'
                    }"
                    
                    
                    />
                </div>
            </div>
            
        </div>
        

    </div>

</template>

<script>

import ProjectCard from './sub_components/ProjectCard.vue'

export default{
    components:{
        ProjectCard,
    }
}

</script>

<style scoped>


</style>
