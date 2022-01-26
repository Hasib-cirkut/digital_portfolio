<template>
        
        <div class="flex flex-col space-y-8">
            <div v-if="!loading" class="flex flex-wrap justify-center items-center space-x-4 space-y-8 px-4">
                <div v-for="item in instaImages" :key="item.id" class="w-2/5">
                    <PersonalCard :mediaUrl="item.media_url" :caption="item.caption"/>
                </div>
            </div>

            <div class="text-center px-8 py-4 font-semibold text-[#faebd7] text-2xl font-mono">

                <a href="https://www.instagram.com/hasib.cirkut/">hasib.cirkut</a>
                
            </div>
        </div>
    
</template>

<script>

import PersonalCard from './sub_components/PersonalCard.vue'

export default {
    data(){
        return{
            instaImages : [],
            loading: true
        }
    },
    components:{
        PersonalCard
    },
    async mounted(){
        let data = await fetch(`https://portfolio-serverless-theta.vercel.app/api`)

        data = await data.json()

        this.instaImages = data

        this.loading = false;
    }
}
</script>

