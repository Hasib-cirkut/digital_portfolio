<template>

  <main class="overflow-x-hidden relative w-full">
  <div id="left" class="fixed w-1/2 bg-gray-900 h-full text-white font-mono p-20">
    <div class="flex flex-col h-full">
        <div class="flex-1 select-none">
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

      <div id="bottom_bar" class="flex space-x-4">

        <div :class="{'text-pink-400' : info.activeBottomTab === 'intro'}">Intro</div>
        <div :class="{'text-pink-400' : info.activeBottomTab === 'project'}">Project</div>
        <div :class="{'text-pink-400' : info.activeBottomTab === 'education'}">Education</div>
        <div :class="{'text-pink-400' : info.activeBottomTab === 'personal'}">Personal</div>

      </div>
    </div>
  </div>

  <!-- <div class="bg-[url('images/bg_blob_1.svg')] absolute w-full h-full bg-no-repeat"> </div>-->
  <div id="right flex-1"
  class="bg-teal-600 float-right w-1/2 space-y-32 overflow-auto scroll-smooth">

    <ProfileCard />

    <Projects />

    <Education />

    <Personal />

    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
    <div class="h-16 w-16 bg-gray-900"></div>
  </div>
</main>

  
  
</template>

<script>

import ProfileCard from './components/ProfileCard.vue'
import Projects from './components/Projects.vue'
import Education from './components/Education.vue'
import Personal from './components/Personal.vue'


export default {

  data(){
    return {
      scrollPos: 0,
      bottomBarClass: '',
      activeBottomTab: ''
    }
  },

  components: {
    ProfileCard,
    Projects,
    Education,
    Personal
  },

  methods:{
  },

  computed:{
    info: function(){
      if(this.scrollPos > -1 && this.scrollPos < 630){
        return {
          label: 'Hello.',
          desc: 'Nice to meet you. My name is Hasibul Huda. I\'m currently working as Junior Software Engineer at WellDev.',
          activeBottomTab: 'intro'
        }
      }
      else if(this.scrollPos > 630 && this.scrollPos < 1400){
      return {
          label: 'Projects.',
          desc: 'I have been developing web apps since my junior years. Here are some of them for you to explore.',
          activeBottomTab: 'project'
        }
      }
      else if(this.scrollPos > 1400 && this.scrollPos < 2200){
      return {
          label: 'Education.',
          desc: 'I\'m an CS graduate from East West University. Some of the major courses I took in University are DS, Algorithm and Machine Learning.',
          activeBottomTab: 'education'
        }
      }
      else
      return {
          label: 'Personal.',
          desc: 'Apart from programming, I like to listen to 60/70\'s rock, read poetry, take photographs',
          activeBottomTab: 'personal'
        }
    }
  },

  created: function() {
    window.addEventListener('scroll', e => this.scrollPos = window.scrollY);
  },
}

</script>
