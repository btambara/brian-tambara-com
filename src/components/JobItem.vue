<script setup lang="ts">
type Job = {
  company: string;
  website: string;
  location: string;
  from: string;
  to: string;
  title: string;
  description: string;
  stack: {
    id: number;
    name: string;
  }[];
};

const details = defineProps<Job>();

function openWebsite() {
  window.location.href = details.website;
}
</script>

<template>
  <v-hover v-slot="{ isHovering, props }">
    <v-card
      variant="elevated"
      :class="{ 'on-hover': isHovering }"
      v-bind="props"
      link
      @click="openWebsite()"
      color="#65474C"
    >
      <v-container fluid>
        <v-row>
          <v-col class="pt-3 text-right" cols="auto">
            <v-card-subtitle>
              {{ details.from }} - {{ details.to }}
            </v-card-subtitle>
          </v-col>
          <v-col class="text-left">
            <v-card-title>
              <a :href="details.website">{{ details.company }}</a>
            </v-card-title>

            <v-card-subtitle>{{ details.location }}</v-card-subtitle>
            <v-card-subtitle>{{ details.title }}</v-card-subtitle>
            <v-card-text>{{ details.description }}</v-card-text>
            <div class="ml-2">
              <v-chip class="ma-1" v-for="tech in details.stack" :key="tech.id"
                >{{ tech.name }}
              </v-chip>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-hover>
</template>

<style scoped>
.on-hover {
  background-color: rgba(255, 255, 255, 0.8);
}
</style>
