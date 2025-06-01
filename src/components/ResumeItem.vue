<script setup lang="ts">
import Job from "./JobItem.vue";
import resume from "../assets/resume.json";
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
            v-for="(item, index) in resume.professional.experience"
            :key=index
          >
            <Job
              :company="item.company"
              :website="item.website"
              :title="item.title"
              :location="item.location.city + ',  ' + item.location.state"
              :from="item.from"
              :to="item.to"
              :description="item.summary"
              :stack="item.stack"
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
