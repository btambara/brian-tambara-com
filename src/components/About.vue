<script setup lang="ts">
</script>

<template>
    <v-container fluid>
      <v-row>
        <v-col>
            <h2 class="text-left">[ About Me ]</h2>
            <p class="text-left">Quality-focused application development professional with a passion for programming. Dedicated to writing elegant code that is reusable, understandable, and easy to maintain. Offer several years of experience in development lifecycle management. Leverage technical expertise in numerous programming languages and platforms - including [Java, Python, and SQL] - to improve user experiences and create breakthrough, innovative applications.</p>
        </v-col>
      </v-row>
      <v-row>
  
        <v-carousel cycle hide-delimiters height="40vh" class="mt-0 gt-0">
          <v-carousel-item>
            <div class="d-flex fill-height justify-center align-center flex-column text-left card ml-16">
                <v-icon class="mb-3" icon="fas fa-terminal" />
                <h4>View time consuming processes and system shortfalls as opportunities to innovate</h4>
                <p>Developed applications to automate time-consuming tasks, increase operational efficiency, and eliminate errors caused by manual intervention.</p>
            </div>
          </v-carousel-item>

          <v-carousel-item>
              <div class="d-flex fill-height justify-center align-center flex-column text-left card ml-16">
                <v-icon class="mb-3" icon="far fa-file-code" />
                <h4>Continuously learn and adapt to rapidly evolving and emerging technologies</h4>
                <p>Automated process for backing up major studio projects at Deluxe Media. Learned Python and PHP to develop a user-friendly and intuitive web interface.</p>
              </div>
          </v-carousel-item>

          <v-carousel-item>
            <div class="d-flex fill-height justify-center align-center flex-column text-left card ml-16">
              <v-icon class="mb-3" icon="fas fa-wrench" />
              <h4>Managed the migration from Python 2 to Python 3 for a client application.</h4>
              <p>Refactored codebase to reflect the latest Python 3 changes. Updated all libraries for compatibility. Added typing to most of the codebase. Wrote unit tests to confirm that the changes work correctly.</p>
            </div>
          </v-carousel-item>
        </v-carousel>
      </v-row>
    </v-container>
  </template>

<style scoped>
.card {
  width:80%
}
</style>