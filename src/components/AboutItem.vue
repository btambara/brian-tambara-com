<script setup lang="ts"></script>

<template>
  <v-container fluid>
    <v-row>
      <v-col class="pt-lg-11 mt-lg-11">
        <div class="mb-3 text-h5 text-left">[ About Me ]</div>
        <div class="text-body-1 text-left">
          <b>Quality-focused application development professional</b> with a
          passion for programming. Dedicated to writing elegant code that is
          <b>reusable, understandable, and easy to maintain</b>. Offer several
          years of experience in development lifecycle management. Leverage
          technical expertise in <b>numerous programming languages</b> and
          platforms - including [Java, Python, and SQL] - to <b>improve</b> user
          experiences and <b>create</b> breakthrough,
          <b>innovative</b> applications.
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-carousel cycle hide-delimiters :show-arrows="false">
        <v-carousel-item>
          <div
            class="px-lg-16 mx-lg-16 d-flex flex-column justify-center align-center"
          >
            <v-icon class="mb-3" icon="fas fa-terminal" color="#C3829D" />
            <div class="font-weight-bold text-left">
              View time consuming processes and system shortfalls as
              opportunities to innovate
            </div>
            <div class="text-body-1 text-left">
              Developed applications to automate time-consuming tasks, increase
              operational efficiency, and eliminate errors caused by manual
              intervention.
            </div>
          </div>
        </v-carousel-item>

        <v-carousel-item>
          <div
            class="px-lg-16 mx-lg-16 d-flex flex-column justify-center align-center"
          >
            <v-icon class="mb-3" icon="far fa-file-code" color="#C3829D" />
            <div class="font-weight-bold text-left">
              Continuously learn and adapt to rapidly evolving and emerging
              technologies
            </div>
            <div class="text-body-1 text-left">
              Automated process for backing up major studio projects at Deluxe
              Media. Learned Python and PHP to develop a user-friendly and
              intuitive web interface.
            </div>
          </div>
        </v-carousel-item>

        <v-carousel-item>
          <div
            class="px-lg-16 mx-lg-16 d-flex flex-column justify-center align-center"
          >
            <v-icon class="mb-3" icon="fas fa-wrench" color="#C3829D" />
            <div class="font-weight-bold text-left">
              Managed the migration from Python 2 to Python 3 for a client
              application.
            </div>
            <div class="text-body-1 text-left">
              Refactored codebase to reflect the latest Python 3 changes.
              Updated all libraries for compatibility. Added typing to most of
              the codebase. Wrote unit tests to confirm that the changes work
              correctly.
            </div>
          </div>
        </v-carousel-item>
      </v-carousel>
    </v-row>
  </v-container>
</template>

<style scoped>
.font-weight-bold {
  color: #d69b43;
}
b {
  color: #c3829d;
}

.text-h5 {
  color: #d69b43;
}
</style>
