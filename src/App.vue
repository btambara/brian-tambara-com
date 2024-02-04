<script setup lang="ts">
import Resume from './components/Resume.vue'
import About from './components/About.vue'
import { ref } from 'vue';

const isAboutShowing = ref(true)
const isResumeShowing = ref(false)

function handleAbout(){
  if(!isAboutShowing.value){
    isAboutShowing.value = true
    isResumeShowing.value = false
  }
}

function handleResume(){
  if(!isResumeShowing.value){
    isAboutShowing.value = false
    isResumeShowing.value = true
  }
}

</script>

<template>
    <v-container>
      <v-row class="h-screen">
        <v-col class="mt-16" cols="5">
          <h1 class="mb-1 text-left">Brian Tambara</h1>
          <h2 class="mb-1 text-left">Software Engineer</h2>

          <p class="text-left">I am a Los Angeles based Software Engineer currently looking for work. My preferred languages for building web applications are Python and Typescript.</p>
          <v-col class="mt-4">
            <v-row>
              <v-btn variant="plain" @click="handleAbout()">
              About
              </v-btn>
            </v-row>

            <v-row>
              <v-btn variant="plain" @click="handleResume()">
              Resume
              </v-btn>
            </v-row>
          </v-col>

          <v-btn href="http://github.com/btambara" icon="fab fa-github" variant="text"></v-btn>
          <v-btn href="mailto:btambara@gmail.com" icon="fas fa-envelope" variant="text"></v-btn>
        </v-col>

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
</style>
