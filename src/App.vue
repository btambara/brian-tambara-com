<script setup lang="ts">
import Resume from './components/Resume.vue'
import About from './components/About.vue'
import { ref } from 'vue';

const isAboutShowing = ref(true)
const isResumeShowing = ref(false)
const variantAbout = ref("text")
const variantResume = ref("plain")

function handleAbout(){
  if(!isAboutShowing.value){
    isAboutShowing.value = true
    isResumeShowing.value = false
    variantResume.value = "plain"
    variantAbout.value = "text"
    scroll(0,0)
  }
}

function handleResume(){
  if(!isResumeShowing.value){
    isAboutShowing.value = false
    isResumeShowing.value = true
    variantResume.value = "text"
    variantAbout.value = "plain"
    scroll(0,0)
  }
}

</script>

<template>
    <v-container>
      <v-row class="h-screen">
        <div class="ma-2 pa-2 fixed">
          <v-col cols="5">
            <div>
              <v-col class="mt-11 intro-pane rounded-lg pa-6">
                <h1 class="text-left text-gold">Brian Tambara</h1>
                <h2 class="text-left">Software Engineer</h2>

                <p class="text-left">I am a Los Angeles based Software Engineer currently looking for work. My preferred languages for building web applications are Python and Typescript.</p>
                <v-col class="mt-4">
                  <v-row>
                    <v-btn :variant="variantAbout" @click="handleAbout()">
                      About
                    </v-btn>
                  </v-row>

                  <v-row>
                    <v-btn :variant="variantResume" @click="handleResume()">
                    Resume
                    </v-btn>
                  </v-row>
                </v-col>
              </v-col>
            </div>

            <v-row class="mt-2 justify-center">
              <v-btn href="http://github.com/btambara" icon="fab fa-github" variant="text"></v-btn>
              <v-btn href="mailto:btambara@gmail.com" icon="fas fa-envelope" variant="text"></v-btn>
            </v-row>
          </v-col>
        </div>
        <v-col>
          <About v-show="isAboutShowing"/>
          <Resume v-show="isResumeShowing" />
        </v-col>
      </v-row>
    </v-container>      
</template>

<style scoped>
.fixed {
  position: fixed;
}
.intro-pane {
  background-color: #65474C;
}

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.text-gold {
  color: #D69B43
}
</style>
