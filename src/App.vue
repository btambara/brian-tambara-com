<script setup lang="ts">
import Resume from "./components/ResumeItem.vue";
import About from "./components/AboutItem.vue";
import { ref } from "vue";

const isAboutShowing = ref(true);
const isResumeShowing = ref(false);
const variantAbout = ref("text");
const variantResume = ref("plain");

function handleAbout() {
  if (!isAboutShowing.value) {
    isAboutShowing.value = true;
    isResumeShowing.value = false;
    variantResume.value = "plain";
    variantAbout.value = "text";
    scroll(0, 0);
  }
}

function handleResume() {
  if (!isResumeShowing.value) {
    isAboutShowing.value = false;
    isResumeShowing.value = true;
    variantResume.value = "text";
    variantAbout.value = "plain";
    scroll(0, 0);
  }
}
</script>

<template>
  <v-container>
    <v-row>
      <v-col
        class="ma-sm-1 mt-md-16 mt-lg-16 mt-xl-10"
        cols="12"
        md="6"
        lg="5"
        xl="5"
      >
        <v-sheet color="#4A4064">
          <v-sheet class="rounded-xl" color="#65474c" elevation="12">
            <div class="ml-8 pt-4 text-h4 text-sm-h3 text-md-h3 text-lg-h3 text-xl-h3 text-left">Brian Tambara</div>
            <div class="ml-9 mb-2 text-h6 text-sm-h5 text-md-h5 text-lg-h5 text-xl-h5 text-left">Software Engineer</div>
            <div class="ml-9 mr-9 text-body-2 text-left">
              I am a Los Angeles based Software Engineer currently looking for
              work. My preferred languages for building web applications are
              Python and Typescript.
            </div>
            <div class="mt-4 pb-4">
              <v-btn :variant="variantAbout" @click="handleAbout()">
                About
              </v-btn>
              <v-btn :variant="variantResume" @click="handleResume()">
                Resume
              </v-btn>
            </div>
          </v-sheet>
          <div class="mt-3">
            <v-btn
              href="http://github.com/btambara"
              icon="fab fa-github"
              variant="text"
            ></v-btn>
            <v-btn
              href="mailto:btambara@gmail.com"
              icon="fas fa-envelope"
              variant="text"
            ></v-btn>
          </div>
        </v-sheet>
      </v-col>
      <v-col>
        <About v-show="isAboutShowing" />
        <Resume v-show="isResumeShowing" />
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.text-sm-h3 {
  color: #d69b43;
}
.text-md-h3 {
  color: #d69b43;
}
.text-lg-h3 {
  color: #d69b43;
}
.text-xl-h3 {
  color: #d69b43;
}
.text-h4 {
  color: #d69b43;
}
</style>
