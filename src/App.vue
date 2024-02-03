<script setup lang="ts">
import Job from './components/Job.vue'
import jobs from './assets/jobs.json'
</script>

<template>
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

</template>

<style scoped>
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
