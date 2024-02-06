<script setup lang="ts">
</script>

<template>
    <v-container fluid>
      <v-row class="justify-end">
        <v-col class="background-4A4064 rounded-lg pl-10" cols="7">
            <h2 class="text-left">[ About Me ]</h2>
            <p class="text-left text-C6CCBD"><b>Quality-focused application development professional</b> with a passion for programming. Dedicated to writing elegant code that is <b>reusable, understandable, and easy to maintain</b>. Offer several years of experience in development lifecycle management. Leverage technical expertise in <b>numerous programming languages</b> and platforms - including [Java, Python, and SQL] - to <b>improve</b> user experiences and <b>create</b> breakthrough, <b>innovative</b> applications.</p>
        </v-col>
      </v-row>
      <v-row class="justify-end">
        <v-carousel cycle hide-delimiters height="40vh" class="w-50 mr-11">
          <v-carousel-item>
            <div class="d-flex fill-height justify-center align-center flex-column text-left card ml-16">
                <v-icon class="mb-3" icon="fas fa-terminal" color="#C3829D"/>
                <h4>View time consuming processes and system shortfalls as opportunities to innovate</h4>
                <p>Developed applications to automate time-consuming tasks, increase operational efficiency, and eliminate errors caused by manual intervention.</p>
            </div>
          </v-carousel-item>

          <v-carousel-item>
              <div class="d-flex fill-height justify-center align-center flex-column text-left card ml-16">
                <v-icon class="mb-3" icon="far fa-file-code" color="#C3829D"/>
                <h4 color="#D69B43">Continuously learn and adapt to rapidly evolving and emerging technologies</h4>
                <p>Automated process for backing up major studio projects at Deluxe Media. Learned Python and PHP to develop a user-friendly and intuitive web interface.</p>
              </div>
          </v-carousel-item>

          <v-carousel-item>
            <div class="d-flex fill-height justify-center align-center flex-column text-left card ml-16">
              <v-icon class="mb-3" icon="fas fa-wrench" color="#C3829D"/>
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
.text-C6CCBD {
  color: #C6CCBD;
}
.background-C6CCBD {
  background-color: #C6CCBD;
}
.background-C3829D {
  background-color: #C3829D;
}
.background-D69B43 {
  background-color: #D69B43;
}
.background-4A4064 {
  background-color: #4A4064;
}
.background-brown {
  background-color: #65474C;
}

b {
  color: #C3829D;  
}

h4 {
  color: #D69B43
}

h2 {
  color: #D69B43
}
</style>