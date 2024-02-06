<script setup lang="ts">
import Job from './Job.vue'
import jobs from '../assets/jobs.json'
</script>

<template>
    <v-container fluid>
      <v-row class="justify-end">
        <v-col cols="7">
          <v-row class="ml-15 mb-0">
                  <v-btn variant="text" append-icon="fas fa-download" href="/Resume_Brian_Tambara.pdf" class="hover-D69B43">View Full Resume</v-btn>
          </v-row>
          <v-timeline density="compact">
            <v-timeline-item dot-color="#C3829D" fill-dot v-for="job in jobs">
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

<style scoped>
a:hover {
  color: #D69B43;
}
</style>