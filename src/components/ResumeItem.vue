<script setup lang="ts">
import Job from "./JobItem.vue";
import jobs from "../assets/jobs.json";
</script>

<template>
  <v-container>
    <v-row class="justify-end">
      <v-col cols="auto" class="mr-2">
        <v-row class="ml-12">
          <div class="text-h5 text-left">[ Resume ]</div>
          <v-btn
            variant="text"
            append-icon="fas fa-download"
            href="/Resume_Brian_Tambara.pdf"
            class="hover-D69B43"
            >Download Resume</v-btn
          >
        </v-row>
        <v-timeline density="compact">
          <v-timeline-item
            dot-color="#C3829D"
            fill-dot
            size="x-small"
            v-for="job in jobs"
            :key="job.id"
          >
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
.text-h5 {
  color: #d69b43;
}
a:hover {
  color: #d69b43;
}
</style>
