<script setup lang="ts">
import Job from './Job.vue'
import jobs from '../assets/jobs.json'
</script>

<template>
    <v-container fluid>
      <v-row>
        <v-col class="ma-10">
          <v-row>
            <h1 class="mb-1 text-left">Brian Tambara</h1>
            <h2 class="mb-1 text-left">Software Engineer</h2>
            <p class="text-left">I am a Los Angeles based Software Engineer currently looking for work. My preferred languages for building web applications are Python and Typescript.</p>
            <v-container>
                <v-row class="mt-1">
                  <v-btn variant="text">
                    About
                  </v-btn>
                </v-row>
  
                <v-row class="mt-4">
                  <v-btn variant="text">
                    Resume
                  </v-btn>
                </v-row>
            </v-container>
   
            <v-divider :thickness="2" class="mt-4"></v-divider>
          </v-row>
          <v-row class="mt-4">
            <v-btn href="http://github.com/btambara" icon="fab fa-github" variant="plain"></v-btn>
            <v-btn href="mailto:btambara@gmail.com" icon="fas fa-envelope" variant="plain"></v-btn>
          </v-row>
        </v-col>
        <v-col>
          <v-row class="ml-15 mb-0">
                  <v-btn variant="text" append-icon="fas fa-download" href="/Resume_Brian_Tambara.pdf">View Full Resume</v-btn>
          </v-row>
          <v-timeline density="compact">
            <v-timeline-item v-for="job in jobs">
                <Job
                :company="job.company"
                :website="job.website"
                :location="job.location"
                :title="job.title"
                :from="job.from"
                :to="job.to"
                :description="job.description"
                :stack="job.stack"
              />
            </v-timeline-item>
          </v-timeline>        
        </v-col>
      </v-row>
    </v-container>
  </template>

<style scoped></style>