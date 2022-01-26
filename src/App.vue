<template>

  <main class="overflow-x-hidden w-full">
  <div id="left" class="hidden xl:flex xl:fixed xl:w-1/2 xl:bg-gray-900 xl:h-full text-white font-mono p-20">
    <div class="flex flex-col h-full">
      <div class="flex flex-col flex-1 select-none space-y-8 pb-8">

            <div class="flex-1 ">
              <div id="label" class="text-4xl text-pink-400 font-bold">
                <p>{{info.label}}</p>
              </div>

              <div id="desc" class="text-2xl font-bold tracking-wider mt-10">
                <p>{{info.desc}}</p>
              </div>

              <div>
                {{scrollPos}}
              </div>
            </div>

            <div v-if="info.showConnect" class="flex space-x-4">

              <div>Github</div>
              <div>LinkedIn</div>
              <div>Twitter</div>
              <div>Facebook</div>

            </div>

      </div>

      

      <div id="bottom_bar" class="flex space-x-4">

        <div :class="{'text-pink-400' : info.activeBottomTab === 'intro'}">Intro</div>
        <div :class="{'text-pink-400' : info.activeBottomTab === 'project'}">Project</div>
        <div :class="{'text-pink-400' : info.activeBottomTab === 'education'}">Education</div>
        <div :class="{'text-pink-400' : info.activeBottomTab === 'personal'}">Personal</div>
        <div :class="{'text-pink-400' : info.activeBottomTab === 'connect'}">Connect</div>

      </div>
    </div>
  </div>

  <div id="right"
    class="bg-teal-600 float-right w-full xl:w-1/2 space-y-12 md:space-y-48 overflow-auto scroll-smooth">

    <ProfileCard />

    <div>
      <p class="flex justify-center md:hidden text-xl uppercase programmer">
        Projects
      </p>

      <Projects />
    </div>


    <div>
      <p class="flex justify-center md:hidden text-xl uppercase programmer">
        Education
      </p>

      <Education />
    </div>

    <div>
      <p class="flex justify-center md:hidden text-xl uppercase programmer">
        Socials
      </p>
      
      <Personal />
    </div>

    

    <Thankyou />
  </div>
</main>

  
  
</template>

<script>

import ProfileCard from './components/ProfileCard.vue'
import Projects from './components/Projects.vue'
import Education from './components/Education.vue'
import Personal from './components/Personal.vue'
import Thankyou from './components/Thankyou.vue'


export default {

  data(){
    return {
      scrollPos: 0,
      bottomBarClass: '',
      activeBottomTab: '',
      instaImages: [],
      showConnect: false
    }
  },

  components: {
    ProfileCard,
    Projects,
    Education,
    Personal,
    Thankyou
  },

  methods:{
  },

  computed:{
    info: function(){
      if(this.scrollPos > -1 && this.scrollPos < 630){
        return {
          label: 'Hello.',
          desc: 'Nice to meet you. My name is Hasibul Huda. I\'m currently working as Junior Software Engineer at WellDev.',
          activeBottomTab: 'intro',
          showConnect: false
        }
      }
      else if(this.scrollPos > 630 && this.scrollPos < 1400){
      return {
          label: 'Projects.',
          desc: 'I have been developing web apps since my junior years. Here are some of them for you to explore.',
          activeBottomTab: 'project',
          showConnect: false
        }
      }
      else if(this.scrollPos > 1400 && this.scrollPos < 2200){
      return {
          label: 'Education.',
          desc: 'I\'m an CS graduate from East West University. Some of the major courses I took in University are DS, Algorithm and Machine Learning.',
          activeBottomTab: 'education',
          showConnect: false
        }
      }

      else if(this.scrollPos > 2200 && this.scrollPos < 3100){
      return {
          label: 'Personal.',
          desc: 'Apart from programming, I like to listen to 60/70\'s rock, read poetry, take photographs',
          activeBottomTab: 'personal',
          showConnect: false
        }
      }

      else
      return {
          label: 'Connect with me.',
          desc: 'You can always reach out to me by using any of the given medium below.',
          activeBottomTab: 'connect',
          showConnect: true
        }
    },

  },

  created: function() {
    window.addEventListener('scroll', e => this.scrollPos = window.scrollY);
  },

  mounted(){
    
  }
}

</script>

<style scoped>
.programmer{
    color: white;
    -webkit-text-fill-color: transparent;
    -webkit-text-stroke-width: 1px;
    -webkit-text-stroke-color: antiquewhite;
}
</style>

